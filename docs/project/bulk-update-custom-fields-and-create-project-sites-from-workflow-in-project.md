---
title: Mettre à jour en bloc des champs personnalisés et créer des sites de projet dans Project Online
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 815131c6-190c-4f29-83bf-c853eee72821
description: Pour aider les clients à tirer le meilleur parti de Project Online et à améliorer l'extensibilité et la flexibilité des services, nous avons ajouté deux méthodes au modèle objet côté client que vous pouvez utiliser dans les flux de travail et les applications Project online.
ms.openlocfilehash: 4de42471cd8c2f12a982447ccffc27ec8104fa31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355359"
---
# <a name="bulk-update-custom-fields-and-create-project-sites-from-a-workflow-in-project-online"></a>Mise à jour en bloc des champs personnalisés et création de sites de projet à partir d’un flux de travail dans Project Online

Pour aider les clients à tirer le meilleur parti de Project Online et à améliorer l'extensibilité et la flexibilité des services, nous avons ajouté deux méthodes au modèle objet côté client que vous pouvez utiliser dans les flux de travail et les applications Project online.
  
|||
|:-----|:-----|
|**UpdateCustomFields** <br/> |Met à jour en bloc les champs personnalisés du projet. Pour Project Online uniquement. Disponible uniquement dans l'API REST.  <br/> |
|**CreateProjectSite** <br/> | Crée un site de projet. Pour Project Online uniquement. Disponible dans l'API REST, le modèle objet client managé et le modèle objet client JavaScript.  <br/> |
   
En plus de fournir davantage de flexibilité, ces méthodes offrent également des améliorations de performances significatives lors de l'enregistrement et de la publication de projets dans un flux de travail. Cet article explique comment utiliser les méthodes dans l'API REST et fournit des instructions pour la création d'un flux de travail qui met à jour les champs personnalisés en bloc et un flux de travail qui crée un site de projet.
  
> [!NOTE]
> Pour en savoir plus sur l'appel des API REST à partir de flux de travail SharePoint 2013, voir [Using SharePoint Rest services from Workflow with post Method](https://mysharepointinsight.blogspot.com/2013/05/using-sharepoint-rest-services-from.mdl) et [Calling the SharePoint 2013 REST API from a SharePoint Designer Workflow](https://sergeluca.wordpress.com/2013/04/09/calling-the-sharepoint-2013-rest-api-from-a-sharepoint-designer-workflow/). 
  
## <a name="bulk-update-project-custom-fields-from-a-workflow"></a>Mettre à jour en bloc des champs personnalisés de projet à partir d'un flux de travail
<a name="BulkUpdateCustomFields"> </a>

Auparavant, les flux de travail ne pouvaient mettre à jour qu'un seul champ personnalisé à la fois. La mise à jour des champs personnalisés de projet un à un peut entraîner une mauvaise expérience de l'utilisateur final lorsque les utilisateurs passent d'une page de détails de projet à une autre. Chaque mise à jour nécessitait une demande de serveur distincte à l'aide de l'action **définir le champ de projet** et la mise à jour de plusieurs champs personnalisés sur un réseau à faible bande passante et à faible bande passante entraînait une charge non négligeable. Pour résoudre ce problème, nous avons ajouté la méthode **UpdateCustomFields** à l'API REST qui vous permet de mettre à jour en bloc des champs personnalisés. Pour utiliser **UpdateCustomFields**, vous devez transmettre un dictionnaire contenant les noms et les valeurs de tous les champs personnalisés que vous souhaitez mettre à jour.
  
La méthode REST se trouve au point de terminaison suivant:
  
`https://<site-url>/_api/ProjectServer/Projects('<guid>')/Draft/UpdateCustomFields()`
  
> [!NOTE]
> Remplacez l' `<site-url>` espace réservé dans les exemples par l'URL de votre site Project Web App (PWA) et `<guid>` l'espace réservé par votre UID de projet. 
  
Cette section décrit comment créer un flux de travail qui met à jour en bloc des champs personnalisés pour un projet. Le flux de travail suit ces étapes principales:
  
- Attendez que le projet que vous souhaitez mettre à jour soit archivé.
    
- Créer un jeu de données qui définit toutes vos mises à jour de champs personnalisés pour le projet
    
- Extraire le projet
    
- Appeler **UpdateCustomFields** pour appliquer les mises à jour de champs personnalisés au projet 
    
- Enregistrer les informations pertinentes dans l'historique des flux de travail (le cas échéant)
    
- Publier le projet
    
- Archiver le projet
    
Le flux de travail final de bout en bout se présente comme suit:
  
![Flux de travail de bout en bout] (media/8c0741f9-7f76-409d-8c00-e7a8c3ddb89f.png "Flux de travail de bout en bout")
  
### <a name="to-create-a-workflow-that-bulk-updates-custom-fields"></a>Pour créer un flux de travail qui met à jour les champs personnalisés en bloc

1. Facultatif. Stockez l'URL complète de votre projet dans une variable que vous pouvez utiliser dans le flux de travail.
    
    ![Stocker l'URL du projet dans une variable] (media/a880c5c6-8e7a-44dd-87e9-7e532169d489.png "Stocker l'URL du projet dans une variable")
  
2. Ajoutez l'action **attendre un événement de projet** dans le flux de travail et sélectionnez l'événement lors de l'archivage d' **un projet** . 
    
    ![Attendre que le projet soit archivé] (media/699aa9c7-b3c9-426e-a775-96993a13559c.png "Attendre que le projet soit archivé")
  
3. Créez un dictionnaire **requestHeader** à l'aide de l'action **générer le dictionnaire** . Vous utiliserez le même en-tête de demande pour tous les appels de service Web dans ce flux de travail. 
    
    ![Créer le dictionnaire requestHeader] (media/83b0aa10-9ab7-43dd-800d-a738bb815876.png "Créer le dictionnaire requestHeader")
  
4. Ajoutez les deux éléments suivants au dictionnaire.
    
    |Nom|Type|Valeur|
    |:-----|:-----|:-----|
    |Accepter  <br/> |String  <br/> |application/JSON; OData = verbose  <br/> |
    |Content-Type  <br/> |String  <br/> |application/JSON; OData = verbose  <br/> |
   
    ![Ajout d'un en-tête Accept] (media/2f2e2016-3c49-4cac-b1e7-f2b8118b840c.png "Ajout d'un en-tête Accept")
  
5. Créez un dictionnaire **requestBody** à l'aide de l'action **générer le dictionnaire** . Ce dictionnaire stocke toutes les mises à jour de champs que vous souhaitez appliquer. 
    
    Chaque mise à jour de champ personnalisé requiert quatre lignes: le type de métadonnées (1), la clé (2), la valeur (3) et le type de valeur (4) du champ.
    
    - **__metadata/type** Type de métadonnées du champ. Cet enregistrement est toujours identique et utilise les valeurs suivantes: 
    
       - Name: customFieldDictionary (i)/__metadata/type (où **i** est l'index de chaque champ personnalisé dans le dictionnaire, en commençant par 0) 
            
       - Type : String
            
       - Valeur: SP. Clévaleur
    
       ![Définition d'une mise à jour de champ personnalisé] (media/a4423493-6603-42ee-ae50-1ef74c5c59bd.png "Définition d'une mise à jour de champ personnalisé")
  
    - **Clé** Nom interne du champ personnalisé, au format: *Custom_ce23fbf43fa0e411941000155d3c8201* 
    
       Vous pouvez trouver le nom interne d'un champ personnalisé en accédant à son point de terminaison **InternalName** :`https://<site-url>/_api/ProjectServer/CustomFields('<guid>')/InternalName`
    
       Si vous avez créé vos champs personnalisés manuellement, les valeurs diffèrent d'un site à l'autres. Si vous envisagez de réutiliser le flux de travail sur plusieurs sites, assurez-vous que les ID de champ personnalisé sont corrects.
    
    - **Value (valeur** ) Valeur à affecter au champ personnalisé. Pour les champs personnalisés qui sont liés à des tables de choix, vous devez utiliser les noms internes des entrées de la table de choix à la place des valeurs réelles de la table de choix. 
    
       Vous pouvez trouver le nom interne de l'entrée de la table de choix au niveau du point de terminaison suivant:`https://<site-url>/_api/ProjectServer/CustomFields('<guid>')/LookupEntries('<guid>')/InternalName`
    
       Si un champ personnalisé de table de choix est configuré pour accepter plusieurs valeurs, utilisez `;#` pour concaténer des valeurs (comme illustré dans l'exemple de dictionnaire ci-dessous). 
    
    - **ValueType** Type du champ personnalisé que vous mettez à jour. 
    
       - Pour les champs texte, durée, indicateur et LookupTable, utilisez EDM. String
    
       - Pour les champs numériques, utilisez EDM. Int32, EDM. double ou tout autre type de numéro OData accepté.
    
       - Pour les champs de date, utilisez EDM. DateTime
    
       Le dictionnaire de l'exemple ci-dessous définit les mises à jour pour trois champs personnalisés. Le premier est pour un champ personnalisé de table de choix à plusieurs valeurs, le second est pour un champ de nombre et le troisième pour un champ de date. Notez le mode d'incrémentation de l'index **customFieldDictionary** . 
    
       > [!NOTE]
       > Ces valeurs sont indiquées à des fins d'illustration uniquement. Les paires clé-valeur que vous utiliserez dépendent de vos données PWA. 
  
       |Nom|Type|Valeur|
       |:-----|:-----|:-----|
       |customFieldDictionary (0)/__metadata/type  <br/> |String  <br/> |Voyant. Clévaleur  <br/> |
       |customFieldDictionary (0)/Key  <br/> |String  <br/> |Ce23fbf43fa0e411941000155d3c8201\_personnalisé  <br/> |
       |customFieldDictionary (0)/value  <br/> |String  <br/> |Entrée\_b9a2fd69279de411940f00155d3c8201; #Entry\_baa2fd69279de411940f00155d3c8201  <br/> |
       |customFieldDictionary (0)/ValueType  <br/> |String  <br/> |Edm.String  <br/> |
       |customFieldDictionary (1)/__metadata/type  <br/> |String  <br/> |Voyant. Clévaleur  <br/> |
       |customFieldDictionary (1)/Key  <br/> |String  <br/> |Custom_c7f114c97098e411940f00155d3c8201  <br/> |
       |customFieldDictionary (1)/value  <br/> |String  <br/> |90,5  <br/> |
       |customFieldDictionary (1)/ValueType  <br/> |String  <br/> |Edm.Double  <br/> |
       |customFieldDictionary (2)/__metadata/type  <br/> |String  <br/> |Voyant. Clévaleur  <br/> |
       |customFieldDictionary (2)/Key  <br/> |String  <br/> |Custom_c6fb67e0b9a1e411941000155d3c8201  <br/> |
       |customFieldDictionary (2)/value  <br/> |String  <br/> |2015-04-01T00:00:00.0000000  <br/> |
       |customFieldDictionary (2)/ValueType  <br/> |String  <br/> |Edm.DateTime  <br/> |
   
       ![Dictionnaire qui définit les mises à jour de champs personnalisés] (media/41a1f18f-a6b2-40ff-904b-437baf962621.png "Dictionnaire qui définit les mises à jour de champs personnalisés")
  
6. Ajoutez une action de **service Web http d'appel** pour extraire le projet. 
    
    ![Appeler la méthode Checkout] (media/8ce56014-0317-419b-afa7-229d05c86885.png "Appeler la méthode Checkout")
  
7. Modifiez les propriétés de l'appel de service Web pour spécifier l'en-tête de la requête. Pour ouvrir la boîte de dialogue **Propriétés** , cliquez avec le bouton droit sur l'action, puis choisissez **Propriétés**.
    
    ![Spécifier l'en-tête de la demande dans les propriétés d'appel de service Web] (media/d81e92b1-43df-42ad-9cd0-a693f93b164e.png "Spécifier l'en-tête de la demande dans les propriétés d'appel de service Web")
  
8. Ajoutez une action de **service Web http Call** pour appeler la méthode **UpdateCustomFields** . 
    
    ![Créer une action de service Web http d'appel] (media/9a73a201-c035-41b4-8798-506ac48b90f8.png "Créer une action de service Web http d'appel")
  
    Notez le `/Draft/` segment dans l'URL du service Web. L'URL complète doit ressembler à ceci:`https://<site-url>/_api/ProjectServer/Projects('<guid>')/Draft/UpdateCustomFields()`
    
    ![Appeler la méthode UpdateCustomFields] (media/03b323f1-8e99-4b18-be18-be505d7cec7e.png "Appeler la méthode UpdateCustomFields")
  
9. Modifiez les propriétés de l'appel de service Web pour lier les paramètres **RequestHeader** et **RequestContent** aux dictionnaires que vous avez créés. Vous pouvez également créer une variable pour stocker le **ResponseContent**.
    
    ![Lier les dictionnaires à l'en-tête et au contenu de la demande] (media/f96bec92-138e-4eab-b1e7-1ab83d0428a5.png "Lier les dictionnaires à l'en-tête et au contenu de la demande")
  
10. Facultatif. Lisez dans le dictionnaire de réponses pour vérifier l'état du travail de file d'attente et consignez les informations dans l'historique des flux de travail.
    
    ![Configuration] de la journalisation (media/7d2f4936-61d7-4906-83e8-7478a5935af5.png "Configuration") de la journalisation
  
11. Ajoutez un appel de service Web au point de terminaison de **publication** pour publier le projet. Utilisez toujours le même en-tête de requête. 
    
    ![Appeler la méthode publish] (media/3b661091-ffae-4d7e-a0bb-5b96a6292731.png "Appeler la méthode publish")
  
    ![Propriétés de l'appel de service Web Publish] (media/6a80a5d3-7e29-4398-993c-f78b3faca8b1.png "Propriétés de l'appel de service Web Publish")
  
12. Ajoutez un appel de service Web final au point de terminaison **checkin** pour vérifier le projet. 
    
    ![Appeler la méthode checkin] (media/430510cb-0774-4911-af7f-b565b83eba0e.png "Appeler la méthode checkin")
  
    ![Propriétés de l'appel de service Web checkin] (media/485f48d6-bbb8-4568-9dc3-aae3218f6bd1.png "Propriétés de l'appel de service Web checkin")

<a name="CreateProjectSite"> </a>

## <a name="create-a-project-site-from-a-workflow"></a>Créer un site de projet à partir d'un flux de travail

Chaque projet peut disposer de ses propres sites SharePoint dédiés où les membres de l'équipe peuvent collaborer, partager des documents, émettre des problèmes, etc. Auparavant, les sites pouvaient uniquement être créés automatiquement lors de la première publication ou manuellement par le responsable de projet dans Project Professionnel ou par l'administrateur dans les paramètres de PWA, ou ils peuvent être désactivés.
  
Nous avons ajouté la méthode **CreateProjectSite** afin que vous puissiez choisir quand créer des sites de projet. Ceci est particulièrement utile pour les organisations qui souhaitent créer automatiquement leurs sites lorsqu'une proposition de projet atteint une étape spécifique dans un flux de travail prédéfini, et non lors de la première publication. Le report de la création d'un site de projet améliore considérablement les performances de création d'un projet. 
  
**Conditions préalables:** Avant de pouvoir utiliser **CreateProjectSite**, le paramètre **permettre aux utilisateurs de choisir** un paramètre doit être défini pour la création de sites de projet dans les paramètres de Project Web **app** > * * **paramètres**>.
  
![Définition de l'option «autoriser les utilisateurs à choisir» dans les paramètres de Project Web App] (media/6c6c8175-eb10-431d-8056-cea55718fdb4.png "Paramètre autoriser les utilisateurs à choisir dans les paramètres de Project Web App")
  
### <a name="to-create-a-workflow-that-creates-a-project-site"></a>Pour créer un flux de travail qui crée un site de projet

1. Créez ou modifiez un flux de travail existant et sélectionnez l'étape où vous souhaitez créer vos sites de projet.
    
2. Créez un dictionnaire **requestHeader** à l'aide de l'action **générer le dictionnaire** . 
    
    ![Créer le dictionnaire requestHeader] (media/83b0aa10-9ab7-43dd-800d-a738bb815876.png "Créer le dictionnaire requestHeader")
  
3. Ajoutez les deux éléments suivants au dictionnaire.
    
    |Nom|Type|Valeur|
    |:-----|:-----|:-----|
    |Accepter  <br/> |String  <br/> |application/JSON; OData = verbose  <br/> |
    |Content-Type  <br/> |String  <br/> |application/JSON; OData = verbose  <br/> |
   
    ![Ajout d'un en-tête Accept] (media/2f2e2016-3c49-4cac-b1e7-f2b8118b840c.png "Ajout d'un en-tête Accept")
  
4. Ajoutez l'action de **service Web http Call** . Modifiez le type de demande afin d'utiliser **post**et définissez l'URL au format suivant:
    
    `https://<site-url>/_api/ProjectServer/Projects('<guid>')/CreateProjectSite('New web name')`
    
    ![Génération de l'URI du point de terminaison CreateProjectSite] (media/42a90a5e-8d1b-4667-a933-785175212847.png "Génération de l'URI du point de terminaison CreateProjectSite")
  
    TransMettez le nom du site de projet à la méthode **CreateProjectSite** sous forme de chaîne. Pour utiliser le nom du projet comme nom de site, transmettez une chaîne vide. Veillez à utiliser des noms uniques de sorte que le prochain site de projet que vous créez fonctionnera. 
    
5. Modifiez les propriétés de l'appel de service Web pour lier le paramètre **RequestHeader** au dictionnaire que vous avez créé. 
    
    ![Liaison du dictionnaire à la demande] (media/61a5a0a8-405f-44eb-b5e7-80b11f7caec3.png "Liaison du dictionnaire à la demande")
  
## <a name="see-also"></a>Voir aussi

- [Tâches de programmation Project](project-programming-tasks.md)
- [Modèle objet côté client (CSOM) pour Project 2013](client-side-object-model-csom-for-project-2013.md)
- [Flux de travail dans SharePoint 2013](https://msdn.microsoft.com/library/e0602371-ae22-44be-8a7e-9e47e9f046d6%28Office.15%29.aspx)
    

