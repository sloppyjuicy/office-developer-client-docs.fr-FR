---
title: Project Architecture et programmabilité de Server 2013
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
f1_keywords:
- architecture
- platform
- Project
- Project architecture
- Project programmability
- Project Server architecture
- Project Server programmability
keywords:
- project 2013, architecture et programmabilité, programmabilité, Project Server,Project 2013, avantages pour EPM, Architecture et Project Server
localization_priority: Normal
ms.assetid: 9ea3b3c1-fb90-454a-b8e6-abc44fca663d
description: Les articles de cette section décrivent l’architecture globale de la solution de gestion Enterprise Project (EPM), qui combine Project Professionnel 2013, Project Server 2013, Project Web App et SharePoint Server 2013.
ms.openlocfilehash: 44cd5a32b8d3de421ffe3b2d9bf0137146bc4c4e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413786"
---
# <a name="project-server-2013-architecture-and-programmability"></a><span data-ttu-id="6029e-104">Project Architecture et programmabilité de Server 2013</span><span class="sxs-lookup"><span data-stu-id="6029e-104">Project Server 2013 architecture and programmability</span></span>

<span data-ttu-id="6029e-105">Les articles de cette section décrivent l’architecture globale de la solution de gestion Enterprise Project (EPM), qui combine Project Professionnel 2013, Project Server 2013, Project Web App et SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6029e-105">The articles in this section describe the overall architecture of the Enterprise Project Management (EPM) solution, which combines Project Professional 2013, Project Server 2013, Project Web App, and SharePoint Server 2013.</span></span>
  
<span data-ttu-id="6029e-106">Project Server 2013 est conçu avec le .NET Framework 4 et est la troisième version majeure de Project Server pour fournir une véritable architecture multitente.</span><span class="sxs-lookup"><span data-stu-id="6029e-106">Project Server 2013 is built with the .NET Framework 4 and is the third major release of Project Server to provide a true multitier architecture.</span></span> <span data-ttu-id="6029e-107">Pour l’accès au cloud, Project Server 2013 implémente un modèle objet côté client (CSOM) et un service OData pour les rapports qui peuvent être utilisés dans les applications web, les applications mobiles et les applications Silverlight.</span><span class="sxs-lookup"><span data-stu-id="6029e-107">For cloud access, Project Server 2013 implements a client-side object model (CSOM) and an OData service for reporting that can be used in web applications, mobile applications, and Silverlight applications.</span></span> <span data-ttu-id="6029e-108">Pour les applications sur site, les clients peuvent utiliser le CSOM ou les services PSI (Project Server Interface).</span><span class="sxs-lookup"><span data-stu-id="6029e-108">For applications on-premises, clients can use either the CSOM or the Project Server Interface (PSI) services.</span></span> 
  
## <a name="introduction-to-project-server-architecture"></a><span data-ttu-id="6029e-109">Présentation de l’architecture Project Server</span><span class="sxs-lookup"><span data-stu-id="6029e-109">Introduction to Project Server architecture</span></span>

<span data-ttu-id="6029e-110">Les rubriques de cette section décrivent l’architecture globale de la solution de gestion Enterprise Project (EPM), qui combine Project Professionnel 2013, Project Server 2013, Project Web App et SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6029e-110">The topics in this section describe the overall architecture of the Enterprise Project Management (EPM) solution, which combines Project Professional 2013, Project Server 2013, Project Web App, and SharePoint Server 2013.</span></span>
  
<span data-ttu-id="6029e-111">Pour l’accès par programme à Project Server, vous devez utiliser le CSOM ou les services PSI avec l’interface WCF (Windows Communication Foundation).</span><span class="sxs-lookup"><span data-stu-id="6029e-111">For programmatic access to Project Server, you should use either the CSOM or the PSI services with the Windows Communication Foundation (WCF) interface.</span></span> <span data-ttu-id="6029e-112">L’interface de service web ASMX de l’interface PSI est Project Server 2013, mais fonctionne toujours.</span><span class="sxs-lookup"><span data-stu-id="6029e-112">The ASMX web service interface of the PSI is deprecated in Project Server 2013, but still works.</span></span> <span data-ttu-id="6029e-113">L’interface PSI permet un accès efficace à l’aide de jeux de données et vous pouvez créer des handlers pour les événements côté serveur.</span><span class="sxs-lookup"><span data-stu-id="6029e-113">The PSI enables efficient access by using datasets and you can create handlers for server-side events.</span></span> <span data-ttu-id="6029e-114">Le modèle CSOM lui-même utilise l’interface PSI pour accéder à la couche Project’objet métier serveur.</span><span class="sxs-lookup"><span data-stu-id="6029e-114">The CSOM itself uses the PSI to access the Project Server business object layer.</span></span> <span data-ttu-id="6029e-115">Au lieu de quatre bases de données Project server, Project Server 2013 utilise une seule base de données dans la couche d’accès aux données.</span><span class="sxs-lookup"><span data-stu-id="6029e-115">Instead of four Project Server databases, Project Server 2013 uses a single database in the data access layer.</span></span>
  
<span data-ttu-id="6029e-116">Project Server 2013 s’intègre de SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6029e-116">Project Server 2013 integrates deeply with SharePoint Server 2013.</span></span> <span data-ttu-id="6029e-117">Le Project d’application peut être associé à d’SharePoint collections de sites dans la batterie de serveurs.</span><span class="sxs-lookup"><span data-stu-id="6029e-117">The Project Application Service can be associated with other SharePoint site collections in the farm.</span></span> <span data-ttu-id="6029e-118">Project Le serveur peut fonctionner avec des listes de tâches SharePoint dans la collection de sites et peut également obtenir un contrôle total sur l’emplacement où Project Server importe et gère les listes de tâches en tant que projets d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="6029e-118">Project Server can operate with and report on SharePoint task lists in the site collection, and can also get full control where Project Server imports and manages the task lists as enterprise projects.</span></span> <span data-ttu-id="6029e-119">Project Le serveur utilise également la version 4 de Windows Workflow Foundation (WF4) et ajoute des activités de flux de travail pour les solutions de gestion de la demande.</span><span class="sxs-lookup"><span data-stu-id="6029e-119">Project Server also uses version 4 of the Windows Workflow Foundation (WF4) and adds workflow activities for Demand Management solutions.</span></span>
  
<span data-ttu-id="6029e-120">Pour plus d’informations sur les nombreuses nouvelles fonctionnalités que Project 2013 fournit aux développeurs et sur les fonctionnalités qui sont dépréciées, voir Mises à jour pour les développeurs dans [Project 2013.](updates-for-developers-in-project-2013.md)</span><span class="sxs-lookup"><span data-stu-id="6029e-120">For a discussion of the many new features that Project 2013 provides for developers, and of the features that are deprecated, see [Updates for developers in Project 2013](updates-for-developers-in-project-2013.md).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="6029e-121">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="6029e-121">In this section</span></span>

<span data-ttu-id="6029e-122">[Project Server 2013 décrit](project-server-2013-architecture.md) les principales parties de la plateforme Project 2013, y compris les clients et les serveurs.</span><span class="sxs-lookup"><span data-stu-id="6029e-122">[Project Server 2013 architecture](project-server-2013-architecture.md) describes the major parts of the Project 2013 platform, including the clients and servers.</span></span> 
  
<span data-ttu-id="6029e-123">[Project Server programmabilité](project-server-programmability.md) décrit les principales fonctionnalités d’extensibilité de Project Server 2013, la personnalisation de Project Web App et la mise à niveau des applications conçues pour les versions précédentes de Project Server.</span><span class="sxs-lookup"><span data-stu-id="6029e-123">[Project Server programmability](project-server-programmability.md) discusses the main extensibility features of Project Server 2013, customization of Project Web App, and upgrading applications that are built for previous Project Server versions.</span></span> 
  
<span data-ttu-id="6029e-124">[Ce que l’interface PSI](what-the-psi-does-and-does-not-do.md) fait et ne fait pas décrit les scénarios dans lequel l’interface PSI peut être utilisée et répertorie les choses que l’interface PSI ne peut pas faire.</span><span class="sxs-lookup"><span data-stu-id="6029e-124">[What the PSI does and does not do](what-the-psi-does-and-does-not-do.md) describes scenarios where the PSI can be used and lists things that the PSI cannot do.</span></span> 
  
<span data-ttu-id="6029e-125">[Ce que le CSOM](what-the-csom-does-and-does-not-do.md) fait et ne fait pas décrit les scénarios dans lequel le CSOM peut être utilisé et répertorie les choses que le CSOM ne peut pas faire.</span><span class="sxs-lookup"><span data-stu-id="6029e-125">[What the CSOM does and does not do](what-the-csom-does-and-does-not-do.md) describes scenarios where the CSOM can be used and lists things that the CSOM cannot do.</span></span> 
  
### <a name="topics-not-covered"></a><span data-ttu-id="6029e-126">Rubriques non couvertes</span><span class="sxs-lookup"><span data-stu-id="6029e-126">Topics not covered</span></span>

<span data-ttu-id="6029e-127">Les articles de la section Architecture et *programmabilité* ne documentent pas les fonctionnalités des clients de bureau Project (Project Standard 2013 et Project Professionnel 2013) ou Project Web App.</span><span class="sxs-lookup"><span data-stu-id="6029e-127">The articles in the  *Architecture and programmability*  section do not document features of the Project desktop clients (Project Standard 2013 and Project Professional 2013) or Project Web App.</span></span> 
  
<span data-ttu-id="6029e-128">Visual Basic pour Applications (VBA) est disponible dans l’éditeur Visual Basic dans Project Standard et Project Professionnel.</span><span class="sxs-lookup"><span data-stu-id="6029e-128">Visual Basic for Applications (VBA) help is available in the Visual Basic editor within Project Standard and Project Professional.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6029e-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6029e-129">See also</span></span>
<span data-ttu-id="6029e-130"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="6029e-130"><a name="bk_addresources"> </a></span></span>

- [<span data-ttu-id="6029e-131">Mises à jour pour les développeurs dans Project 2013</span><span class="sxs-lookup"><span data-stu-id="6029e-131">Updates for developers in Project 2013</span></span>](updates-for-developers-in-project-2013.md)
    
- [<span data-ttu-id="6029e-132">Prise en main du développement de flux de travail Project Server</span><span class="sxs-lookup"><span data-stu-id="6029e-132">Getting started developing Project Server workflows</span></span>](getting-started-developing-project-server-workflows.md)
    

