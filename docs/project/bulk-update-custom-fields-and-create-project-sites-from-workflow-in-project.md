---
title: En bloc des champs personnalisés de mise à jour et créer des sites de projet dans Project Online
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 815131c6-190c-4f29-83bf-c853eee72821
description: Pour aider les clients à tirer le meilleur parti de Project Online et d’améliorer notre service et la flexibilité, nous avons ajouté deux méthodes au modèle objet côté client que vous pouvez utiliser dans des applications Project Online et de flux de travail.
ms.openlocfilehash: 4f8fee5de5efb69f410b78e9ce93b9dc9bb133f3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787811"
---
# <a name="bulk-update-custom-fields-and-create-project-sites-from-a-workflow-in-project-online"></a>Bloc de mise à jour des champs personnalisés et créer des sites de projet à partir d’un flux de travail dans Project Online

Pour aider les clients à tirer le meilleur parti de Project Online et d’améliorer notre service et la flexibilité, nous avons ajouté deux méthodes au modèle objet côté client que vous pouvez utiliser dans des applications Project Online et de flux de travail.
  
|||
|:-----|:-----|
|**UpdateCustomFields** <br/> |Champs personnalisés de projet des mises à jour en bloc. Pour Project Online uniquement. Disponible uniquement dans l’API REST.  <br/> |
|**CreateProjectSite** <br/> | Crée un site de projet. Pour Project Online uniquement. Disponible dans l’API REST, le modèle objet client managé et le modèle d’objet client JavaScript.  <br/> |
   
Outre une plus grande flexibilité, ces méthodes offrent également d’importantes améliorations des performances lors de l’enregistrement et la publication des projets dans un flux de travail. Cet article explique comment utiliser les méthodes de l’API REST et fournit des instructions pour la création d’un flux de travail que des mises à jour en bloc des champs personnalisés et un flux de travail qui crée un site de projet.
  
> [!NOTE]
> Pour en savoir plus sur l’appel d’API REST de flux de travail SharePoint 2013, voir [services REST de SharePoint à l’aide de flux de travail avec la méthode POST](http://mysharepointinsight.blogspot.com/2013/05/using-sharepoint-rest-services-from.mdl) et [appeler l’API Rest SharePoint 2013 à partir d’un flux de travail SharePoint Designer](https://sergeluca.wordpress.com/2013/04/09/calling-the-sharepoint-2013-rest-api-from-a-sharepoint-designer-workflow/). 
  
## <a name="bulk-update-project-custom-fields-from-a-workflow"></a>Champs personnalisés de projet en bloc mise à jour à partir d’un flux de travail
<a name="BulkUpdateCustomFields"> </a>

Auparavant, flux de travail peut uniquement à jour un champ personnalisé à la fois. Mise à jour des champs personnalisés de projet un à la fois peut entraîner une expérience utilisateur médiocre lorsque les utilisateurs la transition entre les Pages de détails de projet. Chaque mise à jour nécessaires une demande de serveur distinct à l’aide de l’action **Définir un champ de projet** , et mise à jour plusieurs champs personnalisés dans une latence élevée, faible bande passante réseau a provoqué une surcharge importante. Pour résoudre ce problème, nous avons ajouté à la méthode **UpdateCustomFields** pour l’API REST que vous permet de que vous en bloc mettre à jour les champs personnalisés. Pour utiliser **UpdateCustomFields**, vous passez un dictionnaire contenant les noms et valeurs de tous les champs personnalisés que vous souhaitez mettre à jour.
  
Vous trouverez la méthode reste au point de terminaison suivant :
  
`https://<site-url>/_api/ProjectServer/Projects('<guid>')/Draft/UpdateCustomFields()`
  
> [!NOTE]
> Remplacez le `<site-url>` espace réservé dans les exemples avec l’URL de votre site Project Web App (PWA) et le `<guid>` espace réservé avec votre projet UID. 
  
Cette section décrit comment créer un flux de travail, en bloc met à jour les champs personnalisés pour un projet. Le flux de travail suit les étapes générales suivantes :
  
- Attendez que le projet que vous souhaitez mettre à jour pour obtenir d’archivage
    
- Créer un jeu de données qui définit toutes vos mises à jour de champ personnalisé pour le projet
    
- Extraire le projet
    
- Appelez **UpdateCustomFields** pour appliquer les mises à jour du champ personnalisé au projet 
    
- Enregistrer des informations pertinentes à la liste d’historique des flux de travail (si nécessaire)
    
- Publier le projet
    
- Archiver le projet
    
Le flux de travail final, de bout en bout ressemble à ceci :
  
![Flux de travail de bout en bout] (media/8c0741f9-7f76-409d-8c00-e7a8c3ddb89f.png "Flux de travail de bout en bout")
  
### <a name="to-create-a-workflow-that-bulk-updates-custom-fields"></a>Pour créer un flux de travail, en bloc met à jour les champs personnalisés

1. Facultatif. Stocker l’URL complète de votre projet dans la variable que vous pouvez utiliser tout au long du flux de travail.
    
    ![Magasin de l’URL du projet dans une variable] (media/a880c5c6-8e7a-44dd-87e9-7e532169d489.png "Magasin de l’URL du projet dans une variable")
  
2. Ajouter l’action **attendre un événement de projet de** flux de travail et choisissez l’événement **lorsqu’un projet est archivé** . 
    
    ![Attendez que le projet à archiver] (media/699aa9c7-b3c9-426e-a775-96993a13559c.png "Attendez que le projet à archiver")
  
3. Créer un dictionnaire **requestHeader** à l’aide de l’action de **génération de dictionnaire** . Vous allez utiliser l’en-tête de demande même pour tous les appels avec le service web dans ce flux de travail. 
    
    ![Créer le dictionnaire requestHeader] (media/83b0aa10-9ab7-43dd-800d-a738bb815876.png "Créer le dictionnaire requestHeader")
  
4. Ajoutez les deux éléments suivants dans le dictionnaire.
    
    |Name|Type|Valeur|
    |:-----|:-----|:-----|
    |Accepter  <br/> |Chaîne  <br/> |application/json ; OData = verbose  <br/> |
    |Content-Type  <br/> |Chaîne  <br/> |application/json ; OData = verbose  <br/> |
   
    ![Ajout d’un en-tête Accept] (media/2f2e2016-3c49-4cac-b1e7-f2b8118b840c.png "Ajout d’un en-tête Accept")
  
5. Créer un dictionnaire **requestBody** à l’aide de l’action de **génération de dictionnaire** . Ce dictionnaire stocke toutes les mises à jour de champ que vous souhaitez appliquer. 
    
    Chaque mise à jour du champ personnalisé nécessite quatre lignes : du champ type de métadonnées (1), la clé (2), valeur (3) et type de valeur (4).
    
    - **__metadata/type** Le type de champ métadonnées. Cet enregistrement est toujours le même et utilise les valeurs suivantes : 
    
       - Nom : customFieldDictionary (i) / __metadata/type (où **i** est l’index de chaque champ personnalisé dans le dictionnaire, en commençant par 0) 
            
       - Type : String
            
       - Valeur : SP KeyValue
    
       ![Définition d’une mise à jour du champ personnalisé] (media/a4423493-6603-42ee-ae50-1ef74c5c59bd.png "Définition d’une mise à jour du champ personnalisé")
  
    - **Clé** Le nom interne du champ personnalisé, au format : *Custom_ce23fbf43fa0e411941000155d3c8201* 
    
       Vous pouvez trouver le nom interne d’un champ personnalisé en accédant à ses **InternalName** du point de terminaison :`https://<site-url>/_api/ProjectServer/CustomFields('<guid>')/InternalName`
    
       Si vous avez créé manuellement vos champs personnalisés, les valeurs varient d’un site. Si vous prévoyez de réutiliser le flux de travail sur plusieurs sites, assurez-vous que l’ID de champ personnalisé sont corrects.
    
    - **Valeur** Valeur à attribuer au champ personnalisé. Pour les champs personnalisés qui sont liées aux tables de choix, vous devez utiliser les noms internes des entrées de table de choix au lieu des valeurs de table de choix réel. 
    
       Vous trouverez le nom interne de l’entrée de table de choix au point de terminaison suivant :`https://<site-url>/_api/ProjectServer/CustomFields('<guid>')/LookupEntries('<guid>')/InternalName`
    
       Si vous avez un champ personnalisé de table de choix configuré pour accepter plusieurs valeurs, utilisez `;#` concaténation des valeurs (comme illustré dans le dictionnaire d’exemple ci-dessous). 
    
    - **ValueType** Le type de champ personnalisé que vous mettez à jour. 
    
       - Pour les champs de texte, la durée, indicateur et LookupTable, utilisez Edm.String
    
       - Pour les champs numérique, utilisez Edm.Int32, Edm.Double ou tout autre accepté OData numéro type
    
       - Pour les champs de Date, utilisez Edm.DateTime
    
       Le dictionnaire de l’exemple ci-dessous définit les mises à jour pour les trois champs personnalisés. Le premier est pour un plusieurs valeur tableau personnalisé champ de recherche, la deuxième est pour un champ numérique et la troisième est pour un champ de date. Note comment incréments index **customFieldDictionary** . 
    
       > [!NOTE]
       > Ces valeurs sont uniquement à des fins d’illustration. Les paires clé-valeur que vous allez utiliser dépendent de vos données PWA. 
  
       |Name|Type|Valeur|
       |:-----|:-----|:-----|
       |type/__metadata/customFieldDictionary (0)  <br/> |Chaîne  <br/> |SP. KeyValue  <br/> |
       |customFieldDictionary (0) / clé  <br/> |Chaîne  <br/> |Personnalisé\_ce23fbf43fa0e411941000155d3c8201  <br/> |
       |customFieldDictionary (0) / valeur  <br/> |Chaîne  <br/> |Entrée\_b9a2fd69279de411940f00155d3c8201 ; #Entry\_baa2fd69279de411940f00155d3c8201  <br/> |
       |customFieldDictionary (0) / ValueType  <br/> |Chaîne  <br/> |Edm.String  <br/> |
       |customFieldDictionary (1) / __metadata/type  <br/> |Chaîne  <br/> |SP. KeyValue  <br/> |
       |customFieldDictionary (1) / clé  <br/> |Chaîne  <br/> |Custom_c7f114c97098e411940f00155d3c8201  <br/> |
       |customFieldDictionary (1) / valeur  <br/> |Chaîne  <br/> |90.5  <br/> |
       |customFieldDictionary (1) / ValueType  <br/> |Chaîne  <br/> |Edm.Double  <br/> |
       |customFieldDictionary (2) / __metadata/type  <br/> |Chaîne  <br/> |SP. KeyValue  <br/> |
       |customFieldDictionary (2) / clé  <br/> |Chaîne  <br/> |Custom_c6fb67e0b9a1e411941000155d3c8201  <br/> |
       |customFieldDictionary (2) / valeur  <br/> |Chaîne  <br/> |2015-04-01T00:00:00.0000000  <br/> |
       |customFieldDictionary (2) / ValueType  <br/> |Chaîne  <br/> |Edm.DateTime  <br/> |
   
       ![Dictionnaire qui définit les mises à jour du champ personnalisé] (media/41a1f18f-a6b2-40ff-904b-437baf962621.png "Dictionnaire qui définit les mises à jour du champ personnalisé")
  
6. Ajouter une action de **Service Web HTTP d’appel** pour extraire le projet. 
    
    ![Appelez la méthode Checkout] (media/8ce56014-0317-419b-afa7-229d05c86885.png "Appelez la méthode Checkout")
  
7. Modifier les propriétés de l’appel de service web pour spécifier l’en-tête de demande. Pour ouvrir la boîte de dialogue **Propriétés** , cliquez sur l’action et choisissez **Propriétés**.
    
    ![Spécifier l’en-tête de demande de service web pour appeler les propriétés] (media/d81e92b1-43df-42ad-9cd0-a693f93b164e.png "Spécifier l’en-tête de demande de service web pour appeler les propriétés")
  
8. Ajouter une action de **Service Web HTTP d’appel** pour appeler la méthode **UpdateCustomFields** . 
    
    ![Créer une action de Service Web HTTP d’appel] (media/9a73a201-c035-41b4-8798-506ac48b90f8.png "Créer une action de Service Web HTTP d’appel")
  
    Remarque la `/Draft/` segment dans l’URL du service web. L’URL complète doit se présenter comme suit :`https://<site-url>/_api/ProjectServer/Projects('<guid>')/Draft/UpdateCustomFields()`
    
    ![Appelez la méthode UpdateCustomFields] (media/03b323f1-8e99-4b18-be18-be505d7cec7e.png "Appelez la méthode UpdateCustomFields")
  
9. Modifier les propriétés de l’appel de service web pour lier les paramètres **RequestHeader** et **RequestContent** aux dictionnaires que vous avez créé. Vous pouvez également créer une nouvelle variable pour stocker le **ResponseContent**.
    
    ![Lier les dictionnaires à l’en-tête de la demande et de contenu] (media/f96bec92-138e-4eab-b1e7-1ab83d0428a5.png "Lier les dictionnaires à l’en-tête de la demande et de contenu")
  
10. Facultatif. Lire à partir du dictionnaire de réponse à l’état du travail en file d’attente et les informations des fichiers journaux dans la liste d’historique de flux de travail.
    
    ![La configuration de journalisation] (media/7d2f4936-61d7-4906-83e8-7478a5935af5.png "La configuration de journalisation")
  
11. Ajoutez un appel au service web au point de terminaison **Publier** pour publier le projet. Toujours utiliser le même en-tête de la demande. 
    
    ![Appelez la méthode de publication] (media/3b661091-ffae-4d7e-a0bb-5b96a6292731.png "Appelez la méthode de publication")
  
    ![Appeler des propriétés pour le service web de publication] (media/6a80a5d3-7e29-4398-993c-f78b3faca8b1.png "Appeler des propriétés pour le service web de publication")
  
12. Ajoutez un appel au service web final au point de terminaison **Checkin** pour archiver le projet. 
    
    ![Appelez la méthode Checkin] (media/430510cb-0774-4911-af7f-b565b83eba0e.png "Appelez la méthode Checkin")
  
    ![Propriétés du service web de consignation des appels] (media/485f48d6-bbb8-4568-9dc3-aae3218f6bd1.png "Propriétés du service web de consignation des appels")

<a name="CreateProjectSite"> </a>

## <a name="create-a-project-site-from-a-workflow"></a>Créer un site de projet à partir d’un flux de travail

Chaque projet peut avoir son propre dédiés sites SharePoint où les membres de l’équipe peuvent collaborer, partager des documents, génère des problèmes et ainsi de suite. Auparavant, les sites peuvent uniquement être créés automatiquement sur tout d’abord publier ou manuellement par le responsable de projet dans Project Professionnel ou par l’administrateur dans PWA paramètres ou qu’ils peuvent être désactivé.
  
Nous avons ajouté la méthode **CreateProjectSite** afin que vous pouvez choisir de créer des sites de projet. Ceci est particulièrement utile pour les entreprises want créer leurs sites automatiquement lorsqu’une proposition de projet atteint une étape spécifique dans un flux de travail prédéfini, au lieu d’abord publier. Report de la création de sites project considérablement améliore les performances de la création d’un projet. 
  
**Requis :** Avant de pouvoir utiliser **CreateProjectSite**, le paramètre **Autoriser les utilisateurs à choisir** doit être défini pour la création du site de projet dans **PWA paramètres** > ** Sites SharePoint connectés ** > **paramètres**.
  
![Définition « Permettre aux utilisateurs de choisir « dans les paramètres PWA] (media/6c6c8175-eb10-431d-8056-cea55718fdb4.png "Paramètre Autoriser les utilisateurs à choisir dans paramètres PWA")
  
### <a name="to-create-a-workflow-that-creates-a-project-site"></a>Pour créer un flux de travail qui crée un site de projet

1. Créer ou modifier un flux de travail existant, puis sélectionnez l’étape où vous souhaitez créer vos sites de projet.
    
2. Créer un dictionnaire **requestHeader** à l’aide de l’action de **génération de dictionnaire** . 
    
    ![Créer le dictionnaire requestHeader] (media/83b0aa10-9ab7-43dd-800d-a738bb815876.png "Créer le dictionnaire requestHeader")
  
3. Ajoutez les deux éléments suivants dans le dictionnaire.
    
    |Name|Type|Valeur|
    |:-----|:-----|:-----|
    |Accepter  <br/> |Chaîne  <br/> |application/json ; OData = verbose  <br/> |
    |Content-Type  <br/> |Chaîne  <br/> |application/json ; OData = verbose  <br/> |
   
    ![Ajout d’un en-tête Accept] (media/2f2e2016-3c49-4cac-b1e7-f2b8118b840c.png "Ajout d’un en-tête Accept")
  
4. Ajoutez l’action **d’Appel HTTP Web Service** . Modifier le type de demande pour utiliser la **publication**et définir l’URL au format suivant :
    
    `https://<site-url>/_api/ProjectServer/Projects('<guid>')/CreateProjectSite('New web name')`
    
    ![Création de l’URI de terminaison CreateProjectSite] (media/42a90a5e-8d1b-4667-a933-785175212847.png "Création de l’URI de terminaison CreateProjectSite")
  
    Passez le nom du site du projet à la méthode **CreateProjectSite** sous forme de chaîne. Pour utiliser le nom du projet comme nom de site, transmettez une chaîne vide. Veillez à utiliser des noms uniques pour le site de projet suivant que vous créez fonctionne. 
    
5. Modifier les propriétés de l’appel de service web pour lier le paramètre **RequestHeader** au dictionnaire que vous avez créé. 
    
    ![Le dictionnaire à la demande de liaison] (media/61a5a0a8-405f-44eb-b5e7-80b11f7caec3.png "Le dictionnaire à la demande de liaison")
  
## <a name="see-also"></a>Voir aussi

- [Tâches de programmation du projet](project-programming-tasks.md)
- [Modèle objet côté client (CSOM) pour Project 2013](client-side-object-model-csom-for-project-2013.md)
- [Flux de travail dans SharePoint 2013](http://msdn.microsoft.com/library/e0602371-ae22-44be-8a7e-9e47e9f046d6%28Office.15%29.aspx)
    

