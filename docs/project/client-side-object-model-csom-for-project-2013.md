---
title: Modèle objet côté client (CSOM) pour Project 2013
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
ms.assetid: 716325eb-b092-4934-921f-84129d0a1f5f
description: Le modèle objet côté client (CSOM) Project Server 2013 met en place une fonctionnalité de serveur commune. Le CSOM Project Server inclut un CSOM Microsoft .NET, un CSOM Microsoft Silverlight, un CSOM Windows Phone 8 et un modèle objet JavaScript (JSOM). En outre, le CSOM inclut un service OData qui active une interface REST. L’interface REST est principalement destinée au développement d’applications sur les plateformes non-Windows, comme iOS et Android.
ms.localizationpriority: high
ms.openlocfilehash: b316f3d776392c2bf00d3213f15129f829f90cea
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63368971"
---
# <a name="client-side-object-model-csom-for-project-2013"></a>Modèle objet côté client (CSOM) pour Project 2013

Le modèle objet côté client (CSOM) Project Server 2013 met en place une fonctionnalité de serveur commune. Le CSOM Project Server inclut un CSOM Microsoft .NET, un CSOM Microsoft Silverlight, un CSOM Windows Phone 8 et un modèle objet JavaScript (JSOM). En outre, le CSOM inclut un service OData qui active une interface REST. L’interface REST est principalement destinée au développement d’applications sur les plateformes non-Windows, comme iOS et Android.
  
> [!NOTE]
> Les solutions pour Microsoft Project Online doivent utiliser le CSOM. Toutefois, les applications locales peuvent utiliser le CSOM ou PSI (Project Server Interface). Si le CSOM inclut la fonctionnalité que vous prévoyez d’utiliser, nous vous recommandons d’utiliser le CSOM pour les nouvelles applications.
  
Dans les extensions CSOM, l’objet **ProjectContext** fournit le point d’entrée aux fonctionnalités et au contenu du serveur. Le modèle CSOM .NET, le modèle CSOM Silverlight et le modèle CSOM Windows Phone utilisent l’objet [Microsoft.ProjectServer.Client.ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx), et le modèle JSOM utilise l’objet **PS.ProjectContext**. Les propriétés **ProjectContext** fournissent un accès direct aux objets Project Server de base dans la collection de sites Project Web App actuelle. Pour plus d’informations sur l’emplacement des assemblys CSOM et du fichier JavaScript, consultez [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx).
  
 **Applications et le modèle de sécurité** Les applications doivent utiliser le modèle CSOM pour les opérations CRUD (créer, lire, mettre à jour, supprimer) avec Project Server 2013 et Project Online. Les applications Project n’utilisent pas le modèle d’authentification d’application uniquement dans SharePoint 2013. Une application Project Server nécessite une demande d’autorisation spécifique indiquant pour qui les commandes sont exécutées.
  
 **Requêtes REST** Vous pouvez créer des requêtes REST du service OData CSOM sans utiliser les métadonnées. Certains outils tiers permettent d’utiliser les assemblys .NET du CSOM pour développer des applications pour d’autres appareils. Par exemple, recherchez sur Internet « Outils de développement .NET multi-plateformes pour iOS ou Android ».
  
> [!NOTE]
> Bien que l’option `$metadata` pour le service de création de rapports **ProjectData** soit valide ( `https://ServerName/pwaName/_api/ProjectData/$metadata`), l’option `$metadata` pour le service **ProjectServer** du CSOM est supprimée dans la version commerciale de Project Server 2013. Pour trouver les objets et les membres du modèle CSOM qui sont disponibles comme points de terminaison REST, reportez-vous à la rubrique relative à la [bibliothèque JavaScript et la référence REST pour Project Server 2013](javascript-library-and-rest-reference-for-project-server-2013.md).
  
Pour voir les entités disponibles dans le CSOM via l’interface REST, vous pouvez utiliser la requête `https://ServerName/pwaName/_api/ProjectServer`. Pour les requêtes REST, l’entité **ProjectServer** met étroitement en miroir les propriétés de l’objet [ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx) dans l’assembly managé Microsoft.ProjectServer.Client.dll et l’objet [PS. ProjectContext](https://msdn.microsoft.com/library/a490b675-a845-ee94-3877-b99ada9bf2b0%28Office.15%29.aspx) dans le modèle JSOM. Par exemple, vous pouvez utiliser votre navigateur pour obtenir des informations du CSOM sur les projets dans Project Web App, les affectations dans un projet spécifié et le nom de tâche d’une affectation spécifiée pour une ressource spécifiée, en utilisant les requêtes suivantes (chaque requête utilise le même préfixe d’URL `https://ServerName/pwaName/_api`). Les GUID sont des exemples de valeurs pour **Project.Id**, **EnterpriseResource.Id** et **Assignment.Id**.
  
```HTML
/ProjectServer/Projects
/ProjectServer/Projects('263fc8d7-427c-e111-92fc-00155d3ba208')/Assignments
/ProjectServer/EnterpriseResources('28eeb2b5-fe74-4efc-aa35-6a64514d1526')/Assignments('a2eafeb5-437c-e111-92fc-00155d3ba208')/Task?$select=Name
```

Contrairement à l’interface OData pour le service **ProjectData**, qui est en lecture seule pour créer des rapports, vous pouvez effectuer des opérations CRUD à l’aide des requêtes REST avec le service **ProjectServer**. Les requêtes REST pour le modèle CSOM Project Server sont conçues principalement pour des plateformes autres que le bureau Windows, comme Windows RT, iOS et Android. Pour les plateformes de serveur et le bureau Windows, telles que Windows 7, Windows 8 et Windows Server 2008 R2, vous pouvez utiliser les assemblys CSOM managés. Pour les applications web, vous pouvez utiliser PS.js pour JavaScript. Pour plus d’informations sur l’exécution d’opérations CRUD à l’aide de requêtes REST, consultez la rubrique [Utiliser les opérations de requête OData dans les demandes REST SharePoint](https://msdn.microsoft.com/library/d4b5c277-ed50-420c-8a9b-860342284b72%28Office.15%29.aspx) dans le kit de développement logiciel SharePoint 2013. Pour plus d’informations sur l’utilisation du service **ProjectData**, consultez la rubrique [Interrogation des flux de données OData des données de création de rapport Project](https://msdn.microsoft.com/library/office/jj163048.aspx).
  
Le tableau 1 répertorie les propriétés **ProjectContext** qui représentent des objets Project Server. Vous pouvez utiliser ces objets pour récupérer d’autres entités Project Server 2013, telles que des affectations et des tâches.
  
**Tableau 1. Propriétés ProjectContext qui permettent d’accéder aux objets Project Server dans le CSOM et le JSOM**

|**CSOM (.NET, Silverlight et Windows Phone)**|**JSOM**|
|:-----|:-----|
|[CustomFields](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.CustomFields.aspx) <br/> |customFields  <br/> |
|[EnterpriseProjectTypes](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EnterpriseProjectTypes.aspx) <br/> |enterpriseProjectTypes  <br/> |
|[EnterpriseResources](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EnterpriseResources.aspx) <br/> |enterpriseResources  <br/> |
|[EntityTypes](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EntityTypes.aspx) <br/> |entityTypes  <br/> |
|[EventHandlers](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EventHandlers.aspx) <br/> |eventHandlers  <br/> |
|[Événements](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Events.aspx) <br/> |événements  <br/> |
|[LookupTables](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.LookupTables.aspx) <br/> |lookupTables  <br/> |
|[Phases](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Phases.aspx) <br/> |phases  <br/> |
|[Projects](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Projects.aspx) <br/> |projects  <br/> |
|[Stages](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Stages.aspx) <br/> |stages  <br/> |
|[WorkflowActivities](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.WorkflowActivities.aspx) <br/> |workflowActivities  <br/> |
|[WorkflowDesigner](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.WorkflowDesigner.aspx) <br/> |workflowDesigner  <br/> |

## <a name="in-this-section"></a>Dans cette section

La section relative à la [prise en main du modèle CSOM Project Server et .NET](getting-started-with-the-project-server-csom-and-net.md) fournit des informations générales sur le modèle CSOM Project Server et .NET, des instructions sur la création d’une extension CSOM .NET simple dans Visual Studio 2012 et des exemples de code connexes.
  
La section relative à la [prise en main du modèle objet JavaScript Project Server 2013](getting-started-with-the-project-server-2013-javascript-object-model.md) fournit des informations générales sur le modèle JSOM Project Server, des instructions sur la création d’une extension JSOM simple dans Visual Studio 2012 et des exemples de code connexes.
  
Consultez également les articles suivants, qui illustrent comment utiliser le CSOM :
  
- [Mise à jour en bloc des champs personnalisés et création de sites de projet à partir d’un flux de travail dans Project Online](bulk-update-custom-fields-and-create-project-sites-from-workflow-in-project.md)

- [Utilisation des projets avec le modèle objet JavaScript](create-retrieve-update-delete-projects-using-project-server-javascript.md)

> [!NOTE]
> Vous pouvez également utiliser Visual Studio 2010 pour le développement de .NET Framework 4 avec le modèle CSOM.
  
## <a name="reference"></a>Référence

[Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx)
  
## <a name="see-also"></a>Voir aussi

[Architecture de Project Server 2013](project-server-2013-architecture.md)
[Choisissez le bon jeu d’API dans SharePoint 2013](https://msdn.microsoft.com/library/f36645da-77c5-47f1-a2ca-13d4b62b320d%28Office.15%29.aspx)
