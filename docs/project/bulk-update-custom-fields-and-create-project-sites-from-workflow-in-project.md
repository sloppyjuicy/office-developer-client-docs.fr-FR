---
title: Mettre à jour en bloc des champs personnalisés et créer des sites de projet dans Project Online
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 815131c6-190c-4f29-83bf-c853eee72821
description: Pour aider les clients à tirer le meilleur parti de Project Online et à améliorer l’extensibilité et la flexibilité de notre service, nous avons ajouté deux méthodes au modèle objet côté client que vous pouvez utiliser dans Project Online applications et workflows.
ms.openlocfilehash: 169b7c0eb46106f2e5b0f78a15ca63b779415e86
ms.sourcegitcommit: b9eed77e21325860cef74e4fb8b86adcc247bc09
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/02/2022
ms.locfileid: "66608532"
---
# <a name="bulk-update-custom-fields-and-create-project-sites-from-a-workflow-in-project-online"></a>Mise à jour en bloc des champs personnalisés et création de sites de projet à partir d’un flux de travail dans Project Online

Pour aider les clients à tirer le meilleur parti de Project Online et à améliorer l’extensibilité et la flexibilité de notre service, nous avons ajouté deux méthodes au modèle objet côté client que vous pouvez utiliser dans Project Online applications et workflows.
  
||Valeur |
|:-----|:-----|
|**UpdateCustomFields** <br/> |Met à jour en bloc les champs personnalisés du projet. Pour Project Online uniquement. Disponible uniquement dans l’API REST. |
|**CreateProjectSite** <br/> | Crée un site Project. Pour Project Online uniquement. Disponible dans l’API REST, le modèle objet client managé et le modèle objet client JavaScript. |

En plus de fournir plus de flexibilité, ces méthodes offrent également des améliorations significatives des performances lors de l’enregistrement et de la publication de projets dans un flux de travail. Cet article explique comment utiliser les méthodes de l’API REST et fournit des instructions pour créer un flux de travail qui met à jour en bloc des champs personnalisés et un flux de travail qui crée un site Project.
  
> [!NOTE]
> Pour en savoir plus sur l’appel d’API REST à partir de flux de travail SharePoint 2013, consultez [Understanding and Using the SharePoint 2013 REST Interface](/archive/msdn-magazine/2013/may/sharepoint-2013-understanding-and-using-the-sharepoint-2013-rest-interface.md) and [Calling the SharePoint 2013 Rest API from a SharePoint Designer Workflow](https://sergeluca.wordpress.com/2013/04/09/calling-the-sharepoint-2013-rest-api-from-a-sharepoint-designer-workflow/).
  
## <a name="bulk-update-project-custom-fields-from-a-workflow"></a>Mettre à jour en bloc les champs personnalisés d’un projet à partir d’un flux de travail

<a name="BulkUpdateCustomFields"> </a>

Auparavant, les flux de travail ne pouvaient mettre à jour qu’un seul champ personnalisé à la fois. La mise à jour des champs personnalisés d’un projet un par un peut entraîner une mauvaise expérience de l’utilisateur final lorsque les utilisateurs passent des pages de détails du projet à l’autre. Chaque mise à jour nécessitait une demande de serveur distincte à l’aide de l’action **Définir le champ de projet** , et la mise à jour de plusieurs champs personnalisés sur un réseau à faible bande passante à latence élevée a entraîné une surcharge non triviale. Pour résoudre ce problème, nous avons ajouté la méthode **UpdateCustomFields** à l’API REST qui vous permet de mettre à jour en bloc des champs personnalisés. Pour utiliser **UpdateCustomFields**, vous transmettez un dictionnaire qui contient les noms et les valeurs de tous les champs personnalisés que vous souhaitez mettre à jour.
  
La méthode REST se trouve au point de terminaison suivant :
  
`https://<site-url>/_api/ProjectServer/Projects('<guid>')/Draft/UpdateCustomFields()`
  
> [!NOTE]
> Remplacez l’espace `<site-url>` réservé dans les exemples par l’URL de votre site Project Web App (PWA) et l’espace `<guid>` réservé par l’UID de votre projet.
  
Cette section explique comment créer un flux de travail qui met à jour en bloc des champs personnalisés pour un projet. Le flux de travail suit ces étapes générales :
  
- Attendez que le projet que vous souhaitez mettre à jour soit archivé

- Créer un jeu de données qui définit toutes vos mises à jour de champs personnalisées pour le projet

- Découvrez le projet

- Appeler **UpdateCustomFields** pour appliquer les mises à jour de champ personnalisées au projet

- Consigner les informations pertinentes dans la liste d’historique des flux de travail (si nécessaire)

- Publier le projet

- Archiver le projet

Le flux de travail final de bout en bout se présente comme suit :
  
![Flux de travail de bout en bout](media/8c0741f9-7f76-409d-8c00-e7a8c3ddb89f.png "Flux de travail de bout en bout")
  
### <a name="to-create-a-workflow-that-bulk-updates-custom-fields"></a>Pour créer un flux de travail qui met à jour en bloc des champs personnalisés

1. Facultatif. Stockez l’URL complète de votre projet dans une variable que vous pouvez utiliser tout au long du flux de travail.

    ![Stocker l’URL du projet dans une variable](media/a880c5c6-8e7a-44dd-87e9-7e532169d489.png "Stocker l’URL du projet dans une variable")
  
2. Ajoutez l’action **Attendre l’événement Project** au flux de travail et choisissez **l’option Quand un projet est archivé dans** l’événement.

    ![Attendre que le projet soit vérifié](media/699aa9c7-b3c9-426e-a775-96993a13559c.png "Attendre que le projet soit vérifié")
  
3. Créez un dictionnaire **requestHeader** à l’aide de l’action **Générer un dictionnaire** . Vous allez utiliser le même en-tête de requête pour tous les appels de service web dans ce flux de travail.

    ![Créer le dictionnaire requestHeader](media/83b0aa10-9ab7-43dd-800d-a738bb815876.png "Créer le dictionnaire requestHeader")
  
4. Ajoutez les deux éléments suivants au dictionnaire.

    |Nom|Type|Valeur|
    |:-----|:-----|:-----|
    |Accepter  <br/> |Chaîne  <br/> |application/json; odata=verbose  <br/> |
    |Content-Type  <br/> |String  <br/> |application/json; odata=verbose  <br/> |

    ![Ajout d’un en-tête Accept](media/2f2e2016-3c49-4cac-b1e7-f2b8118b840c.png "Ajout d’un en-tête Accept")
  
5. Créez un dictionnaire **requestBody** à l’aide de l’action **Générer un dictionnaire** . Ce dictionnaire stocke toutes les mises à jour de champ que vous souhaitez appliquer.

    Chaque mise à jour de champ personnalisée nécessite quatre lignes : le type de métadonnées (1), la clé (2), la valeur (3) et le type de valeur (4).

    - **__metadata/type** Type de métadonnées du champ. Cet enregistrement est toujours le même et utilise les valeurs suivantes :

       - Nom : customFieldDictionary(i)/__metadata/type (où **i** est l’index de chaque champ personnalisé dans le dictionnaire, en commençant par 0)

       - Type : String

       - Valeur : SP. KeyValue

       ![Définition d’une mise à jour de champ personnalisé](media/a4423493-6603-42ee-ae50-1ef74c5c59bd.png "Définition d’une mise à jour de champ personnalisé")
  
    - **Clé** Nom interne du champ personnalisé, au format : *Custom_ce23fbf43fa0e411941000155d3c8201*

       Vous pouvez trouver le nom interne d’un champ personnalisé en accédant au point de terminaison **InternalName** : `https://<site-url>/_api/ProjectServer/CustomFields('<guid>')/InternalName`

       Si vous avez créé vos champs personnalisés manuellement, les valeurs diffèrent d’un site à l’autre. Si vous envisagez de réutiliser le flux de travail sur plusieurs sites, vérifiez que les ID de champ personnalisés sont corrects.

    - **Valeur** Valeur à affecter au champ personnalisé. Pour les champs personnalisés liés aux tables de recherche, vous devez utiliser les noms internes des entrées de table de recherche au lieu des valeurs de table de recherche réelles.

       Vous trouverez le nom interne de l’entrée de table de recherche au point de terminaison suivant : `https://<site-url>/_api/ProjectServer/CustomFields('<guid>')/LookupEntries('<guid>')/InternalName`

       Si vous avez configuré un champ personnalisé de table de recherche pour accepter plusieurs valeurs, utilisez-le `;#` pour concaténer des valeurs (comme indiqué dans l’exemple de dictionnaire ci-dessous).

    - **Valuetype** Type du champ personnalisé que vous mettez à jour.

       - Pour les champs Texte, Durée, Indicateur et LookupTable, utilisez Edm.String

       - Pour les champs Nombre, utilisez Edm.Int32, Edm.Double ou tout autre type de nombre accepté par OData

       - Pour les champs Date, utilisez Edm.DateTime

       L’exemple de dictionnaire ci-dessous définit les mises à jour pour trois champs personnalisés. Le premier concerne un champ personnalisé de table de recherche de valeurs multiples, le second est pour un champ de nombres et le troisième pour un champ de date. Notez comment l’index **customFieldDictionary** s’incrémente.

       > [!NOTE]
       > Ces valeurs sont uniquement à des fins d’illustration. Les paires clé-valeur que vous allez utiliser dépendent de vos données PWA.
  
       |Nom|Type|Valeur|
       |:-----|:-----|:-----|
       |customFieldDictionary(0)/__metadata/type  <br/> |Chaîne  <br/> |SP. KeyValue  <br/> |
       |customFieldDictionary(0)/Key  <br/> |Chaîne  <br/> |Custom\_ce23fbf43fa0e411941000155d3c8201  <br/> |
       |customFieldDictionary(0)/Value  <br/> |Chaîne  <br/> |Entrée\_b9a2fd69279de411940f00155d3c8201;#Entry\_baa2fd69279de411940f0155d3c8201  <br/> |
       |customFieldDictionary(0)/ValueType  <br/> |Chaîne  <br/> |Edm.String  <br/> |
       |customFieldDictionary(1)/__metadata/type  <br/> |String  <br/> |SP. KeyValue  <br/> |
       |customFieldDictionary(1)/Key  <br/> |Chaîne  <br/> |Custom_c7f114c97098e411940f00155d3c8201  <br/> |
       |customFieldDictionary(1)/Value  <br/> |Chaîne  <br/> |90.5  <br/> |
       |customFieldDictionary(1)/ValueType  <br/> |Chaîne  <br/> |Edm.Double  <br/> |
       |customFieldDictionary(2)/__metadata/type  <br/> |Chaîne  <br/> |SP. KeyValue  <br/> |
       |customFieldDictionary(2)/Key  <br/> |Chaîne  <br/> |Custom_c6fb67e0b9a1e411941000155d3c8201  <br/> |
       |customFieldDictionary(2)/Value  <br/> |String  <br/> |2015-04-01T00:00:00  <br/> |
       |customFieldDictionary(2)/ValueType  <br/> |String  <br/> |Edm.DateTime  <br/> |

       ![Dictionnaire définissant les mises à jour de champs personnalisés](media/41a1f18f-a6b2-40ff-904b-437baf962621.png "Dictionnaire définissant les mises à jour de champs personnalisés")
  
6. Ajoutez une action **de service web HTTP d’appel** pour extraire le projet.

    ![Appeler la méthode Checkout](media/8ce56014-0317-419b-afa7-229d05c86885.png "Appeler la méthode Checkout")
  
7. Modifiez les propriétés de l’appel de service web pour spécifier l’en-tête de requête. Pour ouvrir la boîte de dialogue **Propriétés** , cliquez avec le bouton droit sur l’action et choisissez **Propriétés**.

    ![Spécifier l’en-tête de la demande dans les propriétés d’appel de service web](media/d81e92b1-43df-42ad-9cd0-a693f93b164e.png "Spécifier l’en-tête de la demande dans les propriétés d’appel de service web")
  
8. Ajoutez une action **appeler le service web HTTP** pour appeler la méthode **UpdateCustomFields** .

    ![Créer une action Appeler le service web HTTP](media/9a73a201-c035-41b4-8798-506ac48b90f8.png "Créer une action Appeler le service web HTTP")
  
    Notez le `/Draft/` segment dans l’URL du service web. L’URL complète doit ressembler à ceci : `https://<site-url>/_api/ProjectServer/Projects('<guid>')/Draft/UpdateCustomFields()`

    ![Appeler la méthode UpdateCustomFields](media/03b323f1-8e99-4b18-be18-be505d7cec7e.png "Appeler la méthode UpdateCustomFields")
  
9. Modifiez les propriétés de l’appel de service web pour lier les paramètres **RequestHeader** et **RequestContent** aux dictionnaires que vous avez créés. Vous pouvez également créer une variable pour stocker **ResponseContent**.

    ![Lier les dictionnaires au contenu et à l’en-tête de demande](media/f96bec92-138e-4eab-b1e7-1ab83d0428a5.png "Lier les dictionnaires au contenu et à l’en-tête de demande")
  
10. Facultatif. Lisez le dictionnaire de réponses pour vérifier l’état du travail de file d’attente et consigner les informations dans la liste d’historique du flux de travail.

    ![Configuration de la journalisation](media/7d2f4936-61d7-4906-83e8-7478a5935af5.png "Configuration de la journalisation")
  
11. Ajoutez un appel de service web au point de terminaison **Publier** pour publier le projet. Utilisez toujours le même en-tête de requête.

    ![Appeler la méthode Publish](media/3b661091-ffae-4d7e-a0bb-5b96a6292731.png "Appeler la méthode Publish")
  
    ![Propriétés pour l’appel de service web Publish](media/6a80a5d3-7e29-4398-993c-f78b3faca8b1.png "Propriétés pour l’appel de service web Publish")
  
12. Ajoutez un dernier appel de service web au point de terminaison **Checkin** pour vérifier le projet.

    ![Appeler la méthode Checkin](media/430510cb-0774-4911-af7f-b565b83eba0e.png "Appeler la méthode Checkin")
  
    ![Propriétés de l’appel de service web Checkin](media/485f48d6-bbb8-4568-9dc3-aae3218f6bd1.png "Propriétés de l’appel de service web Checkin")

<a name="CreateProjectSite"> </a>

## <a name="create-a-project-site-from-a-workflow"></a>Créer un site Project à partir d’un flux de travail

Chaque projet peut avoir ses propres sites SharePoint dédiés où les membres de l’équipe peuvent collaborer, partager des documents, soulever des problèmes, et ainsi de suite. Auparavant, les sites pouvaient uniquement être créés automatiquement lors de la première publication ou manuellement par le responsable de projet dans Project Professionnel ou par l’administrateur dans les paramètres PWA, ou ils pouvaient être désactivés.
  
Nous avons ajouté la méthode **CreateProjectSite** pour vous permettre de choisir quand créer des sites de projet. Cela est particulièrement utile pour les organisations qui souhaitent créer leurs sites automatiquement lorsqu’une proposition de projet atteint une étape spécifique dans un flux de travail prédéfini, plutôt que lors de la première publication. Le report de la création d’un site de projet améliore considérablement les performances de création d’un projet.
  
**Condition préalable:** Avant de pouvoir utiliser **CreateProjectSite**, le paramètre **Autoriser les utilisateurs à choisir** doit être défini pour la création du site de projet dans **paramètres PWA Paramètres** > **de sites** >  SharePoint **connectés**.
  
![Paramètre « Laisser le choix aux utilisateurs » dans les paramètres PWA](media/6c6c8175-eb10-431d-8056-cea55718fdb4.png "Paramètre Autoriser les utilisateurs à choisir dans les paramètres PWA")
  
### <a name="to-create-a-workflow-that-creates-a-project-site"></a>Pour créer un flux de travail qui crée un site Project

1. Créez ou modifiez un flux de travail existant, puis sélectionnez l’étape dans laquelle vous souhaitez créer vos sites Project.

2. Créez un dictionnaire **requestHeader** à l’aide de l’action **Générer un dictionnaire** .

    ![Créer le dictionnaire requestHeader](media/83b0aa10-9ab7-43dd-800d-a738bb815876.png "Créer le dictionnaire requestHeader")
  
3. Ajoutez les deux éléments suivants au dictionnaire.

    |Nom|Type|Valeur|
    |:-----|:-----|:-----|
    |Accepter  <br/> |Chaîne  <br/> |application/json; odata=verbose  <br/> |
    |Content-Type  <br/> |String  <br/> |application/json; odata=verbose  <br/> |

    ![Ajout d’un en-tête Accept](media/2f2e2016-3c49-4cac-b1e7-f2b8118b840c.png "Ajout d’un en-tête Accept")
  
4. Ajoutez l’action **Appeler le service web HTTP** . Modifiez le type de requête pour utiliser **POST** et définissez l’URL au format suivant :

    `https://<site-url>/_api/ProjectServer/Projects('<guid>')/CreateProjectSite('New web name')`

    ![Construction de l’URI de point de terminaison CreateProjectSite](media/42a90a5e-8d1b-4667-a933-785175212847.png "Construction de l’URI de point de terminaison CreateProjectSite")
  
    Transmettez le nom du site Project à la méthode **CreateProjectSite** sous forme de chaîne. Pour utiliser le nom du projet comme nom de site, passez une chaîne vide. Veillez à utiliser des noms uniques pour que le site de projet suivant que vous créez fonctionne.

5. Modifiez les propriétés de l’appel de service web pour lier le paramètre **RequestHeader** au dictionnaire que vous avez créé.

    ![Liaison du dictionnaire à la demande](media/61a5a0a8-405f-44eb-b5e7-80b11f7caec3.png "Liaison du dictionnaire à la demande")
  
## <a name="see-also"></a>Voir aussi

- [Tâches de programmation Project](project-programming-tasks.md)
- [Modèle objet côté client (CSOM) pour Project 2013](client-side-object-model-csom-for-project-2013.md)
- [Flux de travail dans SharePoint 2013](https://msdn.microsoft.com/library/e0602371-ae22-44be-8a7e-9e47e9f046d6%28Office.15%29.aspx)
