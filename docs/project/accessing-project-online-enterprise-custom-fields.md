---
title: Accès aux champs personnalisés d’entreprise Project Online
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
ms.assetid: 25509631-fa14-49d8-b594-cfacf5355c38
description: 'Project Online est un service Office 365 que les entreprises peuvent étendre afin de répondre à leurs besoins. Une zone d’extension est constituée par les champs personnalisés d’entreprise. Les champs personnalisés d’entreprise sont des champs où des valeurs sont saisies et qui peuvent être ajoutés à des projets, ressources et tâches. Le tableau suivant répertorie les champs personnalisés d’entreprise qui sont associés à des projets, ressources et tâches, et fournit un exemple de valeur pour une instance de ce champ personnalisé d’entreprise :'
localization_priority: Priority
ms.openlocfilehash: 9f754f1446890ae021bf6f7000ffba11e2a2df33
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355082"
---
# <a name="accessing-project-online-enterprise-custom-fields"></a>Accès aux champs personnalisés d’entreprise Project Online

Project Online est un service Office 365 que les entreprises peuvent étendre afin de répondre à leurs besoins. Une zone d’extension est constituée par les champs personnalisés d’entreprise. Les champs personnalisés d’entreprise sont des champs où des valeurs sont saisies et qui peuvent être ajoutés à des projets, ressources et tâches. Le tableau suivant répertorie les champs personnalisés d’entreprise qui sont associés à des projets, ressources et tâches, et fournit un exemple de valeur pour une instance de ce champ personnalisé d’entreprise :
  
|Nom du champ personnalisé d’entreprise|Type de champ personnalisé d’entreprise|Association|Exemple de valeur|
|:-----|:-----|:-----|:-----|
|Justification  <br/> |TEXT  <br/> |Projet  <br/> |Un utilisateur final peut enregistrer des statistiques vitales et des données de santé, avec des résultats qui incluent une évaluation de santé et un plan d’action individualisé vers une meilleure santé.  <br/> |
|Évaluation du risque  <br/> |TEXT  <br/> |Projet  <br/> |Faible  <br/> |
|RETOUR SUR INVESTISSEMENT  <br/> |NUMBER  <br/> |Projet  <br/> |2,10  <br/> |
|Coût total  <br/> |COST  <br/> |Projet  <br/> |1 031 514 $  <br/> |
|Équipe de lancement  <br/> |TEXT  <br/> |Ressources  <br/> |Oui  <br/> |
|Rôle  <br/> |TEXT  <br/> |Ressources  <br/> |Testeur  <br/> |
|État de l’indicateur  <br/> |FLAG  <br/> |Tâche  <br/> |Non  <br/> |
|Intégrité  <br/> |TEXT  <br/> |Tâche  <br/> |Non précisé  <br/> |
   
Les champs personnalisés d’entreprise sont définis au niveau de l’instance Project Web Application (PWA), qui ne fait pas partie d’un projet, d’une ressource ni d’une tâche. Pourtant, ils peuvent être associés à un projet, une ressource ou une tâche. Cet article donne une vue d’ensemble des champs personnalisés à l’aide d’un exemple d’application et porte notamment sur l’extraction de valeurs de champs personnalisés d’entreprise. 
  
Vous pouvez télécharger l’exemple complet dans https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields.
  
En outre, Project Online prend en charge les champs personnalisés locaux comme des entités en lecture seule propres au projet, à la ressource ou à la tâche donnée. Pour plus d’informations sur les champs personnalisés locaux, consultez l’exemple en accédant à https://github.com/OfficeDev/Project-CSOM-Read-Local-CustomFields\.
  
## <a name="background-materials"></a>Documents de référence

Un article précédent relatif au [développement d’une application Project Online à l’aide du modèle objet côté client](developing-a-project-online-application-using-the-client-side-object-model.md) fournit des informations de base et l’orientation initiale pour le développement d’applications à l’aide du modèle objet côté client (CSOM). Consultez cet article pour les éléments suivants :
  
- Informations de base sur Project, éditions autonomes et basées sur le cloud 
    
- Environnement de développement (éditions Visual Studio et bibliothèques de logiciels)
    
- Configuration du projet Visual Studio pour une application .NET à l’aide de la bibliothèque CSOM
    
- Connexion au service Project Online
    
## <a name="preliminaries-class-level-declarations"></a>Déclarations préliminaires (déclarations au niveau de la classe)

La classe pour cette application définit deux éléments de données : le contexte du projet et le dictionnaire pwaECF.
  
L’objet du contexte du projet fait partie du CSOM du projet et connecte l’application et l’instance PWA. Toutes les demandes au service utilisent le contexte du projet.
  
```cs
private static ProjectContext projContext = 
     new ProjectContext("https://Contoso216.sharepoint.com/sites/pwa");

```

Le contexte exige que le point de terminaison de connexion crée une instance dans une application. Le point de terminaison de connexion est l’URL de votre instance PWA. 
  
Le dictionnaire pwaECF stocke les champs personnalisés d’entreprise du projet définis au niveau de l’instance PWA. Le dictionnaire utilise l’élément ECF.InternalName comme clé et l’objet CustomField comme valeur. Le dictionnaire est renseigné dans la méthode ListPWACustomFields, puis utilisé comme référence dans la méthode Main. 
  
```cs
    //Dictionary of ECFs
        static Dictionary<String, CustomField> pwaECF = new Dictionary<string, CustomField>();

```

## <a name="main-method"></a>Méthode Main

La méthode Main gère le flux de l’application. Comme avec d’autres applications qui utilisent le CSOM Project Online, Main initialise le contexte du projet. 
  
1. Récupérer et répertorier les champs personnalisés d’entreprise dans l’instance PWA Project Online.
    
   Cette fonctionnalité est implémentée dans la méthode ListPWACustomFields.
    
2. Récupérer les projets avec des champs personnalisés et des champs non personnalisés.
    
   Lors de la récupération des projets avec des champs personnalisés d’entreprise, la demande de requête au service Project Online doit inclure les éléments suivants : 
    
   - **IncludeCustomFields** &ndash; Cet élément demande au service de renvoyer une collection d’objets PublishedProject où chaque projet publié comporte une extension qui prend en charge les champs personnalisés. Sauf si cet élément est spécifié, Project Online renvoie les objets PublishedProject qui ne comprennent pas de données de champs personnalisés.
    
   - **IncludeCustomFields.CustomFields** &ndash; Cet élément demande au service de renseigner les objets PublishedProject avec des données CustomFields.
    
   La demande suivante spécifie le nom et l’ID du projet, ainsi que l’extension de l’objet pour les champs personnalisés et les valeurs de champ personnalisé.
    
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
    
   Les objets du projet utilisés dans cette application sont le type PublishedProject, car les valeurs sont récupérées et affichées. 
    
   Si vous devez mettre à jour des valeurs de données dans un ou plusieurs projets, le projet en cours de mise à jour sera extrait et l’application utilisera un objet DraftProject pour récupérer les valeurs et mettre à jour le projet.
    
4. Accéder aux entrées de champs personnalisés d’entreprise pour un projet
    
   Chaque instance de champ personnalisé d’entreprise sépare la valeur du champ du reste des informations de champ personnalisé d’entreprise. La valeur du champ est stockée dans le cadre d’une paire clé/valeur. Le reste des informations est stocké dans un objet CustomField.
    
   L’accès aux valeurs de champ personnalisé d’entreprise dans un projet est constitué de deux parties :
    
   - Parcourir la collection CustomFields
    
   - Accéder à l’entrée appropriée en utilisant deux constructions.
    
   Chaque projet stocke les entrées de champ personnalisé d’entreprise associées à deux endroits : une collection CustomFields énumérable et les valeurs du champ dans le cadre de paires clé/valeur. Dans les paires clé/valeur, internalName est la clé et la valeur du champ est la valeur. Utilisez un dictionnaire pour conserver les valeurs du champ et y accéder. 
    
   Les propriétés de champ personnalisé d’entreprise autres que les valeurs du champ sont stockées dans des objets CustomField (un objet par projet). Utilisez une collection CustomFields pour accéder aux champs personnalisés d’entreprise associés à un projet individuel. 
    
5. Chaque projet stocke les champs personnalisés d’entreprise associés dans une collection où chaque champ personnalisé d’entreprise est constitué d’une clé (le nom interne du champ personnalisé d’entreprise) et d’un objet qui conserve la valeur du champ personnalisé d’entreprise. Transférez la collection vers un dictionnaire pour accéder à des entrées individuelles. La déclaration suit.
    
   ```cs
    Dictionary<string, object> projDict = pubProj.IncludeCustomFields.FieldValues;
    
   ```

   La valeur dans une entrée de dictionnaire correspond au type de données du champ personnalisé d’entreprise. L’objet pour chaque champ personnalisé d’entreprise effectue un mappage vers un type parmi d’autres. La plupart des champs personnalisés d’entreprise utilisent des types simples qui s’intègrent dans des variables standard. Le fragment suivant montre qu’un traitement minimal est impliqué pour plusieurs types :
    
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

   Toutefois, la table de choix des valeurs TEXT requiert un traitement supplémentaire. L’application récupère la table de choix appropriée du service et génère l’instance de champ personnalisé d’entreprise (avec une ou plusieurs valeurs) en navigant dans la table de choix. Le fragment de code suivant montre un traitement de champs personnalisés d’entreprise TEXT, y compris ceux ayant des valeurs simples et ceux utilisant des tables de choix : 
    
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

   Cette application génère simplement les valeurs. Toutefois, il est possible de savoir plus en détail ce que les valeurs de données signifient.
    
## <a name="listpwacustomfields"></a>ListPWACustomFields

La méthode ListPWACustomFields récupère et répertorie les champs personnalisés d’entreprise associés à des projets. Cette méthode répertorie les champs personnalisés d’entreprise inscrits sur l’instance PWA qui peuvent être associés à des projets individuels. Le point d’entrée pour accéder aux champs personnalisés d’entreprise utilise l’élément CustomFields du contexte du projet, comme dans la demande de requête suivante :
  
```cs
// Project ECFs
    var allECFields = 
            projContext.LoadQuery(projContext.CustomFields.Include(
            qp => qp.InternalName,
            qp => qp.Name
        ));
    projContext.ExecuteQuery();

```

La méthode ne vérifie pas si un projet utilise un champ personnalisé d’entreprise spécifique.
  
## <a name="see-also"></a>Voir aussi

- [Portail de développement Project](https://developer.microsoft.com/fr-FR/project)
- [Vue d’ensemble : champs personnalisés d’entreprise et tables de choix](https://support.office.com/en-us/article/overview-enterprise-custom-fields-and-lookup-tables-f99db553-0b33-4648-93c0-f6a74637d790?ui=en-us&rs=en-us&ad=us)
- [Champs personnalisés locaux et d’entreprise](https://msdn.microsoft.com/library/office/ms447495(v=office.14).aspx)
- [Ajouter ou modifier des champs personnalisés d’entreprise dans Project Server 2013](https://docs.microsoft.com/project/add-or-edit-enterprise-custom-fields-in-project-server)
    

