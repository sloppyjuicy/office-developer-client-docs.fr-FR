---
title: Accès aux champs personnalisés d’entreprise Project Online
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 25509631-fa14-49d8-b594-cfacf5355c38
description: 'Project Online est un service Office 365 les entreprises peuvent étendre pour répondre aux besoins de l’entreprise. Une zone d’extension est des champs personnalisés d’entreprise (ECFs). ECFs sont des champs de valeur typée qui peuvent être ajoutés à des projets, des ressources et des tâches. Le tableau suivant répertorie les ECFs associer à des projets, des ressources et des tâches et fournit un exemple d’une valeur d’une instance de ce ECF :'
ms.openlocfilehash: 978fdfbf4ba75382ad85b9f92f8ac4df5c7f97c8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401152"
---
# <a name="accessing-project-online-enterprise-custom-fields"></a>Accès aux champs personnalisés d’entreprise Project Online

Project Online est un service Office 365 les entreprises peuvent étendre pour répondre aux besoins de l’entreprise. Une zone d’extension est des champs personnalisés d’entreprise (ECFs). ECFs sont des champs de valeur typée qui peuvent être ajoutés à des projets, des ressources et des tâches. Le tableau suivant répertorie les ECFs associer à des projets, des ressources et des tâches et fournit un exemple d’une valeur d’une instance de ce ECF :
  
|Nom ECF|Type ECF|Association|Exemple de valeur|
|:-----|:-----|:-----|:-----|
|Justification  <br/> |TEXT  <br/> |Projet  <br/> |Un utilisateur final peut enregistrer les statistiques essentielles et des données d’intégrité, avec des résultats qui comprennent une évaluation de l’intégrité et d’une action personnalisée plan vers une meilleure santé.  <br/> |
|Évaluation des risques  <br/> |TEXT  <br/> |Projet  <br/> |Low  <br/> |
|RETOUR SUR INVESTISSEMENT  <br/> |NOMBRE  <br/> |Projet  <br/> |2,10  <br/> |
|Coût total  <br/> |COÛT  <br/> |Projet  <br/> |$1,031,514  <br/> |
|Lancement de l’équipe  <br/> |TEXT  <br/> |Ressources  <br/> |Oui  <br/> |
|Rôle de position  <br/> |TEXT  <br/> |Resources  <br/> |Testeur  <br/> |
|État de l’indicateur  <br/> |INDICATEUR  <br/> |Task  <br/> |Non  <br/> |
|Santé  <br/> |TEXT  <br/> |Task  <br/> |Non spécifié  <br/> |
   
ECFs sont définies au niveau de l’instance Project Web Application (PWA), externe à partir de n’importe quel projet, ressource ou tâche. Ils peuvent encore associés à un projet, la ressource ou la tâche. Cet article fournit un aperçu des champs personnalisés à l’aide d’un exemple d’application d’introduction et se concentre sur la récupération des valeurs ECF. 
  
Vous pouvez télécharger l’exemple complet à https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields.
  
En outre, Project Online prend en charge les champs personnalisés locaux en tant qu’en lecture seule des entités spécifiques pour le projet spécifique, la ressource ou la tâche. Pour plus d’informations sur les champs personnalisés locaux, consultez l’exemple https://github.com/OfficeDev/Project-CSOM-Read-Local-CustomFields\.
  
## <a name="background-materials"></a>Documents d’arrière-plan

Un article précédent, le [développement d’une application Project Online à l’aide du modèle objet côté client](developing-a-project-online-application-using-the-client-side-object-model.md), fournit d’arrière-plan et l’orientation initiale pour le développement d’applications à l’aide de CSOM. Consultez cet article pour les éléments suivants :
  
- Informations générales sur Project, éditions autonomes et en nuage 
    
- Environnement de développement (éditions de Visual Studio et les bibliothèques de logiciels)
    
- Programme d’installation de Visual Studio project pour une application .NET à l’aide de la bibliothèque de CSOM
    
- Connexion au service Project Online
    
## <a name="preliminaries-class-level-declarations"></a>Étapes préliminaires (déclarations au niveau de la classe)

La classe pour cette application définit deux éléments de données : le contexte du projet et le dictionnaire pwaECF.
  
L’objet de contexte de projet fait partie du modèle de projet et connecte l’application et l’instance de PWA. Toutes les demandes au service utilisent le contexte du projet.
  
```cs
private static ProjectContext projContext = 
     new ProjectContext("https://Contoso216.sharepoint.com/sites/pwa");

```

Le contexte nécessite que le point de terminaison de connexion pour créer une instance d’une application. Le point de terminaison de connexion est l’URL de votre instance de PWA. 
  
Le dictionnaire pwaECF stocke le projet ECFs définis au niveau de PWA. Le dictionnaire utilise la ECF. InternalName en tant que la clé et de l’objet CustomField comme valeur. Le dictionnaire est renseigné dans la méthode ListPWACustomFields et ensuite utilisé comme une référence dans la méthode Main. 
  
```cs
    //Dictionary of ECFs
        static Dictionary<String, CustomField> pwaECF = new Dictionary<string, CustomField>();

```

## <a name="main-method"></a>Méthode principale

La méthode Main gère le flux de l’application. Comme avec d’autres applications qui utilisent le Project Online CSOM principal initialise le contexte du projet. 
  
1. Récupérer et répertorier les ECFs dans l’instance de PWA Project Online.
    
   Cette fonctionnalité est implémentée dans la méthode ListPWACustomFields.
    
2. Récupérer les projets avec des champs personnalisés et les champs non personnalisés.
    
   Lors de l’extraction des projets avec ECFs, la demande de requête au service Project Online doit inclure les éléments suivants : 
    
   - **IncludeCustomFields** &ndash; Cet élément demande le service pour retourner une collection de PublishedProjects dont chaque projet publié inclut une extension qui prend en charge les champs personnalisés. Sauf si cet élément est spécifié, Project Online retourne des objets PublishedProject qui ne contiennent pas de données de champ personnalisé.
    
   - **IncludeCustomFields.CustomFields** &ndash; cet élément demande le service pour remplir les objets PublishedProject avec des données CustomFields.
    
   La requête suivante spécifie l’Id de projet ainsi que le nom, ainsi que l’extension de l’objet pour les champs personnalisés et les valeurs de champ personnalisé.
    
   ```cs
        var projBlk = projContext.LoadQuery(
        projContext.Projects.Include(
            p => p.Id, 
            p => p.Name,
            p => p.IncludeCustomFields,
            p => p.IncludeCustomFields.CustomFields
        ));
    
   ```

3. Examiner chaque projet.
    
   Les objets de projet utilisées dans cette application sont le type PublishedProject, car les valeurs sont récupérées et affichées. 
    
   Si vous devez mettre à jour les valeurs de données dans un ou plusieurs projets, le projet en cours de la mise à jour doit être extrait et l’application doit utiliser un objet DraftProject pour récupérer les valeurs et mettre à jour le projet.
    
4. Accès aux entrées ECF pour un projet
    
   Chaque instance ECF sépare le reste des informations ECF la valeur du champ. La valeur du champ est stockée dans le cadre d’une paire clé/valeur. Le reste des informations est stocké dans un objet CustomField.
    
   Accès aux valeurs ECF dans un projet se compose de deux parties :
    
   - Parcourir la collection CustomFields
    
   - Accès à l’entrée appropriée à l’aide de deux constructions.
    
   Chaque projet stocke les entrées ECF associées à deux endroits, une collection CustomFields énumérable et et les valeurs de champ dans le cadre de paires clé/valeur. Dans les paires clé/valeur, internalName est la clé et la valeur du champ est la valeur. Utilisation d’un dictionnaire pour maintenir et accéder aux valeurs de champ. 
    
   Les propriétés ECF, autre que les valeurs de champ, sont stockées dans les objets CustomField, un seul objet par projet. Une collection CustomFields permet d’accéder aux ECFs associés à un projet individuel. 
    
5. Chaque projet stocke les ECFs associés à une collection où chaque entrée ECF se compose d’une clé--le nom interne de l’ECF--et un objet qui conserve la valeur de l’ECF. Transfert de la collection à un dictionnaire pour accéder aux entrées individuelles. La déclaration suivante.
    
   ```cs
    Dictionary<string, object> projDict = pubProj.IncludeCustomFields.FieldValues;
    
   ```

   La valeur dans une entrée de dictionnaire correspond au type de données de l’ECF. L’objet pour chaque ECF correspond à l’un des différents types de. La plupart des ECFs utilisent les types simples qui entrent dans les variables standards. Le fragment suivant montre que le traitement minimal est impliqué pour plusieurs types de :
    
   ```cs
    switch (cf.FieldType)
    {
        case CustomFieldType.COST:
            decimal costValue = (decimal)oVal;
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                costValue.ToString("C"));
            break;
        case CustomFieldType.DATE:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
        case CustomFieldType.FINISHDATE:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
        case CustomFieldType.DURATION:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
        case CustomFieldType.FLAG:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
        case CustomFieldType.NUMBER:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
    
   ```

   La table de choix de valeurs de texte, toutefois, requiert un traitement supplémentaire. L’application extrait la table de choix approprié du service et renvoie l’instance ECF (avec des valeurs uniques ou multiples) en parcourant la table de choix. Le fragment de code suivant illustre le traitement de texte ECFs, y compris ceux avec des valeurs simples et ceux qui utilisent des tables de choix : 
    
   ```cs
    case CustomFieldType.TEXT:
        if (!cf.LookupTable.ServerObjectIsNull.HasValue ||
            (cf.LookupTable.ServerObjectIsNull.HasValue && 
            cf.LookupTable.ServerObjectIsNull.Value))
        { //No lookup table
            Console.WriteLine("\tFieldType:\t{0}\n\tText:\t{1}", cf.FieldType, 
                oVal.ToString());
        }
        else
        { //Lookup table
            Console.WriteLine("\tFieldType:\t{0} - using Lookup Table", cf.FieldType);
            String[] entries = (String[])oVal;
            foreach (String entry in entries)
            {
                var luEntry = projContext.LoadQuery(cf.LookupTable.Entries
                    .Where(e => e.InternalName == entry));
                projContext.ExecuteQuery();
                Console.WriteLine("\tLookup Value:\t{0}", luEntry.First().FullValue);  
            }
        }
        break;
    
   ```

   Cette application renvoie simplement la valeur (s) ; Toutefois, il est possible d’obtenir davantage de signification dans les valeurs de données.
    
## <a name="listpwacustomfields"></a>ListPWACustomFields

La méthode ListPWACustomFields récupère et répertorie les ECFs associés aux projets. Cette méthode répertorie les ECFs inscrits sur l’instance de PWA qui peut être associé à des projets individuels. Le point d’entrée pour accéder aux ECFs utilise l’élément CustomFields du contexte du projet, comme illustré à la demande de requête suivante :
  
```cs
// Project ECFs
    var allECFields = 
            projContext.LoadQuery(projContext.CustomFields.Include(
            qp => qp.InternalName,
            qp => qp.Name
        ));
    projContext.ExecuteQuery();

```

La méthode ne vérifie pas si un projet utilise un ECF spécifique.
  
## <a name="see-also"></a>Voir aussi

- [Portail de développement Project](https://developer.microsoft.com/en-us/project)
- [Vue d’ensemble : Tables de choix et champs personnalisés d’entreprise](https://support.office.com/en-us/article/overview-enterprise-custom-fields-and-lookup-tables-f99db553-0b33-4648-93c0-f6a74637d790?ui=en-us&rs=en-us&ad=us)
- [Local et champs personnalisés d’entreprise](https://msdn.microsoft.com/library/office/ms447495(v=office.14).aspx)
- [Ajouter ou modifier des champs personnalisés d’entreprise dans Project Server 2013](https://docs.microsoft.com/project/add-or-edit-enterprise-custom-fields-in-project-server)
    

