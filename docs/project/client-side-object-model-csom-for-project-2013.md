---
title: Modèle objet côté client (CSOM) pour Project 2013
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 716325eb-b092-4934-921f-84129d0a1f5f
description: Le modèle objet côté client de Project Server 2013 (CSOM) implémente les fonctionnalités communes du serveur. Project Server CSOM inclut un modèle de Microsoft .NET, un Microsoft Silverlight CSOM, un modèle de 8 Windows Phone et un modèle d’objet JavaScript (JSOM). En outre, le modèle CSOM inclut un service OData qui permet à l’interface REST. L’interface REST est destiné principalement pour le développement d’applications sur les plateformes autres que Windows iOS et Android.
ms.openlocfilehash: a17dc816cd2033ff0057821ef029f0163881f9ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787787"
---
# <a name="client-side-object-model-csom-for-project-2013"></a>Modèle objet côté client (CSOM) pour Project 2013

Le modèle objet côté client de Project Server 2013 (CSOM) implémente les fonctionnalités communes du serveur. Project Server CSOM inclut un modèle de Microsoft .NET, un Microsoft Silverlight CSOM, un modèle de 8 Windows Phone et un modèle d’objet JavaScript (JSOM). En outre, le modèle CSOM inclut un service OData qui permet à l’interface REST. L’interface REST est destiné principalement pour le développement d’applications sur les plateformes autres que Windows iOS et Android.
  
> [!NOTE]
> Solutions pour Project Online doivent utiliser le modèle CSOM. Toutefois, les applications de locaux peuvent utiliser le modèle CSOM ou l’Interface de Project Server (PSI). Si le modèle inclut les fonctionnalités que vous prévoyez d’utiliser, nous vous recommandons d’utiliser le modèle CSOM pour les nouvelles applications. 
  
Extensions de modèle, l’objet **ProjectContext** fournit le point d’entrée et le contenu du serveur. Le modèle CSOM .NET, CSOM Silverlight et Windows Phone CSOM utilisent l’objet [Microsoft.ProjectServer.Client.ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx) et le JSOM utilise le **PM. ProjectContext** objet. Propriétés **ProjectContext** fournissent un accès direct aux objets de Project Server core dans la collection de sites Project Web App en cours. Pour plus d’informations sur l’emplacement des assemblys CSOM et le fichier JavaScript, voir [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) . 
  
 **Applications et le modèle de sécurité** Les applications doivent utiliser le modèle CSOM pour CRUD (créer, lire, mettre à jour, supprimer) des opérations avec Project Server 2013 et Project Online. Applications Project n’utilisent pas le modèle d’authentification d’application uniquement dans SharePoint 2013. Une application Project Server requiert une étendue de demande d’autorisation spécifique qui indique au nom duquel les commandes sont en cours d’exécution. 
  
 **Requêtes REST** Vous pouvez créer des requêtes REST du service OData CSOM sans utiliser les métadonnées. Certains des outils tiers activer à l’aide d’assemblys .NET pour CSOM pour développer des applications pour d’autres périphériques. Par exemple, recherchez sur Internet pour « multiplateforme outils de développement .NET pour iOS ou Android. » 
  
> [!NOTE]
> Bien que le `$metadata` option pour la **ProjectData** reporting service valide ( `http://ServerName/pwaName/_api/ProjectData/$metadata`), la `$metadata` option pour le service **ProjectServer** de CSOM est supprimé dans la version de Project Server 2013. Pour rechercher les objets CSOM et les membres qui sont disponibles sous forme de points de terminaison REST, consultez [bibliothèque JavaScript et référence REST pour Project Server 2013](javascript-library-and-rest-reference-for-project-server-2013.md). 
  
Pour voir les entités disponibles dans le modèle CSOM par le biais de l’interface REST, vous pouvez utiliser la `http://ServerName/pwaName/_api/ProjectServer` requête. Pour les requêtes REST, l’entité **ProjectServer** reflète les propriétés de l’objet [ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx) dans l’assembly Microsoft.ProjectServer.Client.dll gérées et le [PM. ProjectContext](http://msdn.microsoft.com/library/a490b675-a845-ee94-3877-b99ada9bf2b0%28Office.15%29.aspx) objet dans le JSOM. Par exemple, vous pouvez utiliser votre navigateur pour obtenir des informations à partir du modèle CSOM sur les projets dans Project Web App, les affectations dans un projet spécifié et le nom de la tâche d’une affectation spécifiée d’une ressource spécifiée, à l’aide de requêtes suivantes (chaque requête utilise le même `http://ServerName/pwaName/_api` préfixe d’URL). Les GUID sont des exemples de valeurs pour **Project.Id**, **EnterpriseResource.Id**et **Assignment.Id**.
  
```HTML
/ProjectServer/Projects
/ProjectServer/Projects('263fc8d7-427c-e111-92fc-00155d3ba208')/Assignments
/ProjectServer/EnterpriseResources('28eeb2b5-fe74-4efc-aa35-6a64514d1526')/Assignments('a2eafeb5-437c-e111-92fc-00155d3ba208')/Task?$select=Name
```

Contrairement à l’interface OData pour le service **ProjectData** , qui est en lecture seule pour la création de rapports, vous pouvez effectuer des opérations CRUD à l’aide de requêtes REST avec le service **ProjectServer** . Requêtes REST pour Project Server CSOM sont adressent principalement aux plateformes autres que le bureau Windows, tels que Windows RT, iOS et Android. Pour les plateformes de serveur et de bureau Windows, tels que Windows 7, Windows 8 et Windows Server 2008 R2, vous pouvez utiliser les assemblys CSOM géré. Pour les applications web, vous pouvez utiliser PS.js pour JavaScript. Pour plus d’informations sur les opérations CRUD à l’aide de requêtes REST, consultez la rubrique [des opérations de requête OData utilisés dans les requêtes REST SharePoint](http://msdn.microsoft.com/library/d4b5c277-ed50-420c-8a9b-860342284b72%28Office.15%29.aspx) dans le Kit de développement SharePoint 2013. Pour plus d’informations sur l’utilisation du service **ProjectData** , voir [OData interrogation des flux de données de création de rapports Project](https://msdn.microsoft.com/en-us/library/office/jj163048.aspx).
  
Le tableau 1 répertorie les propriétés **ProjectContext** qui représentent des objets Project Server. Vous pouvez utiliser ces objets pour récupérer d’autres entités de Project Server 2013, telles que des tâches et affectations. 
  
**Le tableau 1. Propriétés ProjectContext qui fournissent l’accès aux objets Project Server CSOM et JSOM**

|**CSOM (.NET, Silverlight et Windows Phone)**|**JSOM**|
|:-----|:-----|
|[CustomFields](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.CustomFields.aspx) <br/> |customFields  <br/> |
|[EnterpriseProjectTypes](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EnterpriseProjectTypes.aspx) <br/> |enterpriseProjectTypes  <br/> |
|[EnterpriseResources](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EnterpriseResources.aspx) <br/> |enterpriseResources  <br/> |
|[EntityTypes](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EntityTypes.aspx) <br/> |entityTypes  <br/> |
|[EventHandlers](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EventHandlers.aspx) <br/> |eventHandlers  <br/> |
|[Événements](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Events.aspx) <br/> |events  <br/> |
|[Tables de recherche](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.LookupTables.aspx) <br/> |tables de recherche  <br/> |
|[Phases](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Phases.aspx) <br/> |phases  <br/> |
|[Projets](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Projects.aspx) <br/> |projects  <br/> |
|[Étapes](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Stages.aspx) <br/> |stages  <br/> |
|[WorkflowActivities](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.WorkflowActivities.aspx) <br/> |workflowActivities  <br/> |
|[WorkflowDesigner](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.WorkflowDesigner.aspx) <br/> |workflowDesigner  <br/> |
   
## <a name="in-this-section"></a>Dans cette section

[Mise en route avec Project Server CSOM et .NET](getting-started-with-the-project-server-csom-and-net.md) fournit des informations générales sur le Project Server CSOM et .NET, des instructions sur la création d’une simple extension du modèle CSOM .NET dans Visual Studio 2012 et des exemples de code prise en charge. 
  
[Mise en route avec le modèle objet JavaScript de Project Server 2013](getting-started-with-the-project-server-2013-javascript-object-model.md) fournit des informations générales sur le JSOM Server Project, des instructions sur la création d’une extension JSOM simple dans Visual Studio 2012 et des exemples de code prise en charge. 
  
Consultez également les articles suivants, qui illustrent comment utiliser le CSOM :
  
- [Bloc de mise à jour des champs personnalisés et créer des sites de projet à partir d’un flux de travail dans Project Online](bulk-update-custom-fields-and-create-project-sites-from-workflow-in-project.md)
    
- [Travailler avec des projets à l’aide du modèle objet JavaScript](create-retrieve-update-delete-projects-using-project-server-javascript.md)
    
> [!NOTE]
> Vous pouvez également utiliser Visual Studio 2010 pour le développement de .NET Framework 4 avec le modèle CSOM. 
  
## <a name="reference"></a>R�f�rence

[Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx)
  
## <a name="see-also"></a>Voir aussi



[Architecture de Project Server 2013](project-server-2013-architecture.md)


[Choisir l'ensemble d'API approprié dans SharePoint 2013](http://msdn.microsoft.com/library/f36645da-77c5-47f1-a2ca-13d4b62b320d%28Office.15%29.aspx)

