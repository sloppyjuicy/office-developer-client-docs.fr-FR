---
title: Mettre à jour en bloc des champs personnalisés et créer des sites de projet dans Project Online
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 815131c6-190c-4f29-83bf-c853eee72821
description: Pour aider les clients à utiliser au mieux les Project Online et à améliorer l’extensibilité et la flexibilité de nos services, nous avons ajouté deux méthodes au modèle objet côté client que vous pouvez utiliser dans les flux de travail et les applications Project Online.
ms.openlocfilehash: aa5eb1355dfc9e0595337a76307b280c728885e4
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62779636"
---
# <a name="bulk-update-custom-fields-and-create-project-sites-from-a-workflow-in-project-online"></a>Mise à jour en bloc des champs personnalisés et création de sites de projet à partir d’un flux de travail dans Project Online

Pour aider les clients à utiliser au mieux les Project Online et à améliorer l’extensibilité et la flexibilité de nos services, nous avons ajouté deux méthodes au modèle objet côté client que vous pouvez utiliser dans les flux de travail et les applications Project Online.
  
|||
|:-----|:-----|
|**UpdateCustomFields** <br/> |Met à jour en bloc les champs personnalisés de projet. Par Project Online uniquement. Disponible uniquement dans l’API REST. |
|**CreateProjectSite** <br/> | Crée un Project site. Par Project Online uniquement. Disponible dans l’API REST, le modèle objet client géré et le modèle objet client JavaScript. |
   
En plus de fournir plus de flexibilité, ces méthodes offrent également des améliorations significatives en matière de performances lors de l’enregistrement et de la publication de projets dans un flux de travail. Cet article explique comment utiliser les méthodes dans l’API REST et fournit des instructions pour la création d’un flux de travail qui met à jour en bloc des champs personnalisés et un flux de travail qui crée un site Project web.
  
> [!NOTE]
> Pour en savoir plus sur l’appel d’API REST à partir de flux de travail SharePoint 2013, voir Utilisation des [services REST SharePoint](https://mysharepointinsight.blogspot.com/2013/05/using-sharepoint-rest-services-from.mdl) à partir d’un flux de travail avec la méthode POST et appel de l’API [rest SharePoint 2013](https://sergeluca.wordpress.com/2013/04/09/calling-the-sharepoint-2013-rest-api-from-a-sharepoint-designer-workflow/) à partir d’un flux de travail SharePoint Designer. 
  
## <a name="bulk-update-project-custom-fields-from-a-workflow"></a>Mettre à jour en bloc des champs personnalisés de projet à partir d’un flux de travail
<a name="BulkUpdateCustomFields"> </a>

Auparavant, les flux de travail ne pouvaient mettre à jour qu’un seul champ personnalisé à la fois. La mise à jour des champs personnalisés de projet un par un peut entraîner une expérience médiocre pour l’utilisateur final lorsque les utilisateurs passe d’Project pages de détails. Chaque mise à jour nécessitait une demande de serveur distincte à l’aide de l’action Définir un champ **Project**, et la mise à jour de plusieurs champs personnalisés sur un réseau à faible bande passante à latence élevée a entraîné une surcharge non triviale. Pour résoudre ce problème, nous avons ajouté la méthode **UpdateCustomFields** à l’API REST qui vous permet de mettre à jour en bloc des champs personnalisés. Pour utiliser **UpdateCustomFields**, vous passez un dictionnaire qui contient les noms et les valeurs de tous les champs personnalisés que vous souhaitez mettre à jour.
  
La méthode REST se trouve au point de terminaison suivant :
  
`https://<site-url>/_api/ProjectServer/Projects('<guid>')/Draft/UpdateCustomFields()`
  
> [!NOTE]
> Remplacez l’espace `<site-url>` réservé dans les exemples par l’URL de votre site `<guid>` Project Web App (PWA) et l’espace réservé par l’UID de votre projet. 
  
Cette section explique comment créer un flux de travail qui met à jour en bloc les champs personnalisés d’un projet. Le flux de travail suit les étapes de haut niveau suivantes :
  
- Attendre que le projet que vous souhaitez mettre à jour soit enregistré
    
- Créer un jeu de données qui définit toutes vos mises à jour de champ personnalisé pour le projet
    
- Consulter le projet
    
- Appeler **UpdateCustomFields pour** appliquer les mises à jour de champ personnalisé au projet 
    
- Journal des informations pertinentes dans l’historique du flux de travail (si nécessaire)
    
- Publier le projet
    
- Enregistrer le projet
    
Le flux de travail final de bout en bout se ressemble :
  
![Flux de travail de bout en bout](media/8c0741f9-7f76-409d-8c00-e7a8c3ddb89f.png "Flux de travail de bout en bout")
  
### <a name="to-create-a-workflow-that-bulk-updates-custom-fields"></a>Pour créer un flux de travail qui met à jour en bloc des champs personnalisés

1. Facultatif. Stockez l’URL complète de votre projet dans une variable que vous pouvez utiliser tout au long du flux de travail.
    
    ![Stocker l’URL du projet dans une variable](media/a880c5c6-8e7a-44dd-87e9-7e532169d489.png "Stocker l’URL du projet dans une variable")
  
2. Ajoutez **l’action Attendre Project événement** au flux de travail et choisissez **l’événement** Lorsqu’un projet est vérifié. 
    
    ![Attendre que le projet soit vérifié](media/699aa9c7-b3c9-426e-a775-96993a13559c.png "Attendre que le projet soit vérifié")
  
3. Créez **un dictionnaire requestHeader** à l’aide de **l’action Créer un dictionnaire** . Vous utiliserez le même en-tête de requête pour tous les appels de service web dans ce flux de travail. 
    
    ![Créer le dictionnaire requestHeader](media/83b0aa10-9ab7-43dd-800d-a738bb815876.png "Créer le dictionnaire requestHeader")
  
4. Ajoutez les deux éléments suivants au dictionnaire.
    
    |Nom|Type|Valeur|
    |:-----|:-----|:-----|
    |Accepter  <br/> |String  <br/> |application/json; odata=verbose  <br/> |
    |Content-Type  <br/> |String  <br/> |application/json; odata=verbose  <br/> |
   
    ![Ajout d’un en-tête Accept](media/2f2e2016-3c49-4cac-b1e7-f2b8118b840c.png "Ajout d’un en-tête Accept")
  
5. Créez **un dictionnaire requestBody** à l’aide de **l’action Créer un dictionnaire** . Ce dictionnaire stocke toutes les mises à jour de champ que vous souhaitez appliquer. 
    
    Chaque mise à jour de champ personnalisé nécessite quatre lignes : le (1) type de métadonnées du champ, (2) clé, (3) valeur et (4) type de valeur.
    
    - **__metadata/type** Type de métadonnées du champ. Cet enregistrement est toujours le même et utilise les valeurs suivantes : 
    
       - Nom : customFieldDictionary(i)/__metadata/type (où **i** est l’index de chaque champ personnalisé dans le dictionnaire, en commençant par 0) 
            
       - Type : String
            
       - Valeur : SP. KeyValue
    
       ![Définition d’une mise à jour de champ personnalisé](media/a4423493-6603-42ee-ae50-1ef74c5c59bd.png "Définition d’une mise à jour de champ personnalisé")
  
    - **Clé** Nom interne du champ personnalisé, au format : *Custom_ce23fbf43fa0e411941000155d3c8201* 
    
       Vous pouvez trouver le nom interne d’un champ personnalisé en naviguant jusqu’à son point de terminaison **InternalName** : `https://<site-url>/_api/ProjectServer/CustomFields('<guid>')/InternalName`
    
       Si vous avez créé manuellement vos champs personnalisés, les valeurs diffèrent d’un site à l’autre. Si vous envisagez de réutiliser le flux de travail sur plusieurs sites, assurez-vous que les ID de champ personnalisé sont corrects.
    
    - **Valeur** Valeur à affecter au champ personnalisé. Pour les champs personnalisés liés à des tables de recherche, vous devez utiliser les noms internes des entrées de table de recherche au lieu des valeurs réelles de la table de recherche. 
    
       Le nom interne de l’entrée de table de recherche se trouve au point de terminaison suivant : `https://<site-url>/_api/ProjectServer/CustomFields('<guid>')/LookupEntries('<guid>')/InternalName`
    
       Si vous avez une table de choix définie pour accepter plusieurs valeurs,  `;#` utilisez cette opération pour concaténer des valeurs (comme illustré dans l’exemple de dictionnaire ci-dessous). 
    
    - **ValueType** Type du champ personnalisé que vous êtes en train de mettre à jour. 
    
       - Pour les champs Texte, Durée, Indicateur et LookupTable, utilisez Edm.String
    
       - Pour les champs Number, utilisez Edm.Int32, Edm.Double ou tout autre type de numéro accepté OData
    
       - Pour les champs Date, utilisez Edm.DateTime
    
       L’exemple de dictionnaire ci-dessous définit les mises à jour de trois champs personnalisés. Le premier est pour un champ personnalisé de table de choix à valeurs multiples, le second pour un champ de nombres et le troisième pour un champ de date. Notez comment **l’index customFieldDictionary** est incrémenté. 
    
       > [!NOTE]
       > Ces valeurs sont uniquement à des fins d’illustration. Les paires clé-valeur que vous utiliserez dépendent de vos PWA données. 
  
       |Nom|Type|Valeur|
       |:-----|:-----|:-----|
       |customFieldDictionary(0)/__metadata/type  <br/> |String  <br/> |SP. KeyValue  <br/> |
       |customFieldDictionary(0)/Key  <br/> |String  <br/> |Customce23fbf43fa0e411941000155d3c8201\_  <br/> |
       |customFieldDictionary(0)/Value  <br/> |String  <br/> |Entryb9a2fd69279de411940f00155d3c8201\_;#Entry\_ baa2fd69279de411940f00155d3c8201  <br/> |
       |customFieldDictionary(0)/ValueType  <br/> |String  <br/> |Edm.String  <br/> |
       |customFieldDictionary(1)/__metadata/type  <br/> |String  <br/> |SP. KeyValue  <br/> |
       |customFieldDictionary(1)/Key  <br/> |String  <br/> |Custom_c7f114c97098e411940f00155d3c8201  <br/> |
       |customFieldDictionary(1)/Value  <br/> |String  <br/> |90.5  <br/> |
       |customFieldDictionary(1)/ValueType  <br/> |String  <br/> |Edm.Double  <br/> |
       |customFieldDictionary(2)/__metadata/type  <br/> |String  <br/> |SP. KeyValue  <br/> |
       |customFieldDictionary(2)/Key  <br/> |String  <br/> |Custom_c6fb67e0b9a1e411941000155d3c8201  <br/> |
       |customFieldDictionary(2)/Value  <br/> |String  <br/> |2015-04-01T00:00:00  <br/> |
       |customFieldDictionary(2)/ValueType  <br/> |String  <br/> |Edm.DateTime  <br/> |
   
       ![Dictionnaire définissant les mises à jour de champs personnalisés](media/41a1f18f-a6b2-40ff-904b-437baf962621.png "Dictionnaire définissant les mises à jour de champs personnalisés")
  
6. Ajoutez une action **appeler le service Web HTTP** pour vérifier le projet. 
    
    ![Appeler la méthode Checkout](media/8ce56014-0317-419b-afa7-229d05c86885.png "Appeler la méthode Checkout")
  
7. Modifiez les propriétés de l’appel de service web pour spécifier l’en-tête de la demande. Pour ouvrir la boîte **de dialogue Propriétés** , cliquez avec le bouton droit sur l’action et choisissez **Propriétés**.
    
    ![Spécifier l’en-tête de la demande dans les propriétés d’appel de service web](media/d81e92b1-43df-42ad-9cd0-a693f93b164e.png "Spécifier l’en-tête de la demande dans les propriétés d’appel de service web")
  
8. Ajoutez une action **appeler le service Web HTTP** pour appeler la **méthode UpdateCustomFields** . 
    
    ![Créer une action Appeler le service web HTTP](media/9a73a201-c035-41b4-8798-506ac48b90f8.png "Créer une action Appeler le service web HTTP")
  
    Notez le  `/Draft/` segment dans l’URL du service web. L’URL complète doit ressembler à ceci : `https://<site-url>/_api/ProjectServer/Projects('<guid>')/Draft/UpdateCustomFields()`
    
    ![Appeler la méthode UpdateCustomFields](media/03b323f1-8e99-4b18-be18-be505d7cec7e.png "Appeler la méthode UpdateCustomFields")
  
9. Modifiez les propriétés de l’appel de service web pour lier les paramètres **RequestHeader** et **RequestContent** aux dictionnaires que vous avez créés. Vous pouvez également créer une variable pour stocker **le ResponseContent**.
    
    ![Lier les dictionnaires au contenu et à l’en-tête de demande](media/f96bec92-138e-4eab-b1e7-1ab83d0428a5.png "Lier les dictionnaires au contenu et à l’en-tête de demande")
  
10. Facultatif. Lisez le dictionnaire de réponses pour vérifier l’état du travail en file d’attente et enregistrez les informations dans l’historique du flux de travail.
    
    ![Configuration de la journalisation](media/7d2f4936-61d7-4906-83e8-7478a5935af5.png "Configuration de la journalisation")
  
11. Ajoutez un appel de service web au point **de** terminaison Publier pour publier le projet. Utilisez toujours le même en-tête de requête. 
    
    ![Appeler la méthode Publish](media/3b661091-ffae-4d7e-a0bb-5b96a6292731.png "Appeler la méthode Publish")
  
    ![Propriétés pour l’appel de service web Publish](media/6a80a5d3-7e29-4398-993c-f78b3faca8b1.png "Propriétés pour l’appel de service web Publish")
  
12. Ajoutez un dernier appel de service web au point de terminaison **d’enregistrement** pour vérifier le projet. 
    
    ![Appeler la méthode Checkin](media/430510cb-0774-4911-af7f-b565b83eba0e.png "Appeler la méthode Checkin")
  
    ![Propriétés de l’appel de service web Checkin](media/485f48d6-bbb8-4568-9dc3-aae3218f6bd1.png "Propriétés de l’appel de service web Checkin")

<a name="CreateProjectSite"> </a>

## <a name="create-a-project-site-from-a-workflow"></a>Créer un site Project à partir d’un flux de travail

Chaque projet peut avoir ses propres sites SharePoint où les membres de l’équipe peuvent collaborer, partager des documents, lever des problèmes, etc. Auparavant, les sites pouvaient uniquement être créés automatiquement lors de la première publication ou manuellement par le responsable de projet dans Project Professionnel ou par l’administrateur dans les paramètres PWA, ou ils pouvaient être désactivés.
  
Nous avons ajouté la **méthode CreateProjectSite** pour vous aider à choisir quand créer des sites de projet. Ceci est particulièrement utile pour les organisations qui souhaitent créer leurs sites automatiquement lorsqu’une proposition de projet atteint une étape spécifique dans un flux de travail prédéfiny, plutôt que lors de la première publication. Le report de la création d’un site de projet améliore considérablement les performances de création d’un projet. 
  
**Conditions préalables :** Avant de pouvoir utiliser **CreateProjectSite**, le  paramètre Autoriser les utilisateurs à choisir doit être définie pour la création de site de projet dans **PWA Paramètres** > ** Connected SharePoint Sites ** > **Paramètres**.
  
![Paramètre « Laisser le choix aux utilisateurs » dans les paramètres PWA](media/6c6c8175-eb10-431d-8056-cea55718fdb4.png "Paramètre Autoriser les utilisateurs à choisir dans PWA paramètres")
  
### <a name="to-create-a-workflow-that-creates-a-project-site"></a>Pour créer un flux de travail qui crée un site Project site

1. Créez ou modifiez un flux de travail existant et sélectionnez l’étape à laquelle vous souhaitez créer Project sites.
    
2. Créez **un dictionnaire requestHeader** à l’aide de **l’action Créer un dictionnaire** . 
    
    ![Créer le dictionnaire requestHeader](media/83b0aa10-9ab7-43dd-800d-a738bb815876.png "Créer le dictionnaire requestHeader")
  
3. Ajoutez les deux éléments suivants au dictionnaire.
    
    |Nom|Type|Valeur|
    |:-----|:-----|:-----|
    |Accepter  <br/> |String  <br/> |application/json; odata=verbose  <br/> |
    |Content-Type  <br/> |String  <br/> |application/json; odata=verbose  <br/> |
   
    ![Ajout d’un en-tête Accept](media/2f2e2016-3c49-4cac-b1e7-f2b8118b840c.png "Ajout d’un en-tête Accept")
  
4. Ajoutez **l’action Appeler le service Web HTTP** . Modifiez le type de requête pour utiliser **POST** et définissez l’URL au format suivant :
    
    `https://<site-url>/_api/ProjectServer/Projects('<guid>')/CreateProjectSite('New web name')`
    
    ![Construction de l’URI de point de terminaison CreateProjectSite](media/42a90a5e-8d1b-4667-a933-785175212847.png "Construction de l’URI de point de terminaison CreateProjectSite")
  
    Passez le nom du site Project à la **méthode CreateProjectSite** en tant que chaîne. Pour utiliser le nom du projet comme nom de site, passez une chaîne vide. N’oubliez pas d’utiliser des noms uniques pour que le site de projet suivant que vous créez fonctionne. 
    
5. Modifiez les propriétés de l’appel de service web pour lier le **paramètre RequestHeader** au dictionnaire que vous avez créé. 
    
    ![Liaison du dictionnaire à la demande](media/61a5a0a8-405f-44eb-b5e7-80b11f7caec3.png "Liaison du dictionnaire à la demande")
  
## <a name="see-also"></a>Voir aussi

- [Tâches de programmation Project](project-programming-tasks.md)
- [Modèle objet côté client (CSOM) pour Project 2013](client-side-object-model-csom-for-project-2013.md)
- [Flux de travail dans SharePoint 2013](https://msdn.microsoft.com/library/e0602371-ae22-44be-8a7e-9e47e9f046d6%28Office.15%29.aspx)
    

