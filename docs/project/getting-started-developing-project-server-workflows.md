---
title: Prise en main du développement de flux de travail Project Server
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 735bbb04-a8c1-46c0-a346-42050f0ac9b1
description: Les processus de gestion de la demande dans Project Server 2013 incluent des flux de travail qui vous aident à gérer les propositions de projet et les analyses de portefeuilles. Cette section contient des articles qui montrent comment créer des flux de travail pour Project Server.
ms.openlocfilehash: 0a09022e63528f50ee4f0c8bd69bd6c34c5d8753
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344470"
---
# <a name="getting-started-developing-project-server-workflows"></a><span data-ttu-id="5c4e9-104">Prise en main du développement de flux de travail Project Server</span><span class="sxs-lookup"><span data-stu-id="5c4e9-104">Getting started developing Project Server workflows</span></span>

<span data-ttu-id="5c4e9-105">Les processus de gestion de la demande dans Project Server 2013 incluent des flux de travail qui vous aident à gérer les propositions de projet et les analyses de portefeuilles.</span><span class="sxs-lookup"><span data-stu-id="5c4e9-105">Demand management processes in Project Server 2013 include workflows that help you manage project proposals and portfolio analyses.</span></span> <span data-ttu-id="5c4e9-106">Cette section contient des articles qui montrent comment créer des flux de travail pour Project Server.</span><span class="sxs-lookup"><span data-stu-id="5c4e9-106">This section includes articles that show how to create workflows for Project Server.</span></span>
  
<span data-ttu-id="5c4e9-107">Les flux de travail Project Server 2013 utilisent la plateforme de flux de travail SharePoint Server 2013, qui est basée sur la version 4 de Windows Workflow Foundation (WF4).</span><span class="sxs-lookup"><span data-stu-id="5c4e9-107">Project Server 2013 workflows use the SharePoint Server 2013 workflow platform, which is built on version 4 of Windows Workflow Foundation (WF4).</span></span> <span data-ttu-id="5c4e9-108">Les flux de travail WF4 sont déclaratifs, ce qui signifie que l'outil de conception de flux de travail enregistre les étapes du flux de travail, les actions, les conditions et d'autres éléments dans le code XAML, qui est interprété au moment de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="5c4e9-108">WF4-based workflows are declarative, which means that the workflow design tool saves workflow stages, actions, conditions, and other elements to XAML code, which is interpreted at run-time.</span></span> <span data-ttu-id="5c4e9-109">Vous pouvez utiliser SharePoint Designer 2013 ou Visual Studio 2012 pour créer des flux de travail déclaratifs.</span><span class="sxs-lookup"><span data-stu-id="5c4e9-109">You can use either SharePoint Designer 2013 or Visual Studio 2012 to create declarative workflows.</span></span> <span data-ttu-id="5c4e9-110">Un flux de travail nécessite le moteur d'exécution du client Workflow Manager 1,0, qui peut se trouver sur un serveur local pour les solutions locales ou sur un serveur distant pour les solutions Project online.</span><span class="sxs-lookup"><span data-stu-id="5c4e9-110">A workflow requires the Workflow Manager Client 1.0 execution engine, which can be on a local server for on-premises solutions or on a remote server for Project Online solutions.</span></span>
  
<span data-ttu-id="5c4e9-111">Vous pouvez utiliser SharePoint Designer 2013 pour créer des flux de travail déclaratifs relativement simples.</span><span class="sxs-lookup"><span data-stu-id="5c4e9-111">You can use SharePoint Designer 2013 to create relatively simple declarative workflows.</span></span> <span data-ttu-id="5c4e9-112">Pour les flux de travail complexes et les modèles de flux de travail qui peuvent être réutilisés, vous pouvez utiliser Visual Studio 2012 pour développer et déboguer des flux de travail pour Project Web App.</span><span class="sxs-lookup"><span data-stu-id="5c4e9-112">For complex workflows, and workflow templates that can be reused, you can use Visual Studio 2012 to develop and debug workflows for Project Web App.</span></span> <span data-ttu-id="5c4e9-113">Pour plus d'informations, consultez la rubrique [création de flux de travail de projet à l'aide de Visual Studio 2012](https://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx).</span><span class="sxs-lookup"><span data-stu-id="5c4e9-113">For more information, see [Creating Project Workflows using Visual Studio 2012](https://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx).</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="5c4e9-114">Utilisez une installation de test de Project Server, pas une installation de production, pour développer et tester des flux de travail.</span><span class="sxs-lookup"><span data-stu-id="5c4e9-114">Use a test installation of Project Server, not a production installation, to develop and test workflows.</span></span> <span data-ttu-id="5c4e9-115">Les flux de travail qui sont développés pour les versions précommerciales de Project Server 2013 doivent être testés pour la version commerciale et devront peut-être être de nouveau créés et redéployés.</span><span class="sxs-lookup"><span data-stu-id="5c4e9-115">Workflows that are developed for pre-release versions of Project Server 2013 must be tested for the release version, and may have to be created again and redeployed.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="5c4e9-116">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="5c4e9-116">In this section</span></span>

[<span data-ttu-id="5c4e9-117">Créer un flux de travail Project Server pour la gestion de la demande</span><span class="sxs-lookup"><span data-stu-id="5c4e9-117">Create a Project Server workflow for Demand Management</span></span>](create-a-project-server-workflow-for-demand-management.md)
  
## <a name="see-also"></a><span data-ttu-id="5c4e9-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c4e9-118">See also</span></span>



[<span data-ttu-id="5c4e9-119">Mettre à jour en bloc des champs personnalisés et créer des sites de projet à partir d'un flux de travail Project Online</span><span class="sxs-lookup"><span data-stu-id="5c4e9-119">Bulk update custom fields and create project sites from a Project Online workflow</span></span>](bulk-update-custom-fields-and-create-project-sites-from-workflow-in-project.md)


[<span data-ttu-id="5c4e9-120">Développement de flux de travail dans SharePoint Designer 2013 et Visio 2013</span><span class="sxs-lookup"><span data-stu-id="5c4e9-120">Workflow development in SharePoint Designer 2013 and Visio 2013</span></span>](https://msdn.microsoft.com/library/jj163272%28office.15%29.aspx)
  
[<span data-ttu-id="5c4e9-121">Nouveautés des flux de travail pour SharePoint 2013</span><span class="sxs-lookup"><span data-stu-id="5c4e9-121">What's new in workflows for SharePoint 2013</span></span>](https://msdn.microsoft.com/library/jj163177.aspx)
  
[<span data-ttu-id="5c4e9-122">Développer des flux de travail SharePoint 2013 à l'aide de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5c4e9-122">Develop SharePoint 2013 workflows using Visual Studio</span></span>](https://msdn.microsoft.com/library/jj163199.aspx)
  
[<span data-ttu-id="5c4e9-123">Création de flux de travail de projet à l'aide de Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="5c4e9-123">Creating Project Workflows using Visual Studio 2012</span></span>](https://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx)
  
[<span data-ttu-id="5c4e9-124">Windows Workflow Foundation</span><span class="sxs-lookup"><span data-stu-id="5c4e9-124">Windows Workflow Foundation</span></span>](https://msdn.microsoft.com/library/dd489441.aspx)
  
[<span data-ttu-id="5c4e9-125">Présentation de Windows Workflow Foundation (WF) dans .NET 4 pour les développeurs</span><span class="sxs-lookup"><span data-stu-id="5c4e9-125">A developer's introduction to Windows Workflow Foundation (WF) in .NET 4</span></span>](https://msdn.microsoft.com/library/ee342461.aspx)
  
[<span data-ttu-id="5c4e9-126">Guide de l'Guide de la gestion de la demande (livre blanc)</span><span class="sxs-lookup"><span data-stu-id="5c4e9-126">Hitchhiker's guide to demand management (white paper)</span></span>](https://msdn.microsoft.com/library/ff973112.aspx)

