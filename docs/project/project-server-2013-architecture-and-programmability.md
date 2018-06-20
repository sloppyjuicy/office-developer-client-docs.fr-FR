---
title: Architecture de Project Server 2013 et programmabilité
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
- Project 2013, les avantages liés à la programmabilité, programmabilité, Project Server, Project 2013 et architecture pour Project Server, l’Architecture et EPM
localization_priority: Normal
ms.assetid: 9ea3b3c1-fb90-454a-b8e6-abc44fca663d
description: Les articles de cette section expliquent l’architecture globale de la solution Enterprise Project Management (EPM), qui combine Project Professional 2013, Project Server 2013, Project Web App et SharePoint Server 2013.
ms.openlocfilehash: 6b5ab94968dbb996a370e0e5abb89813f5e41ef7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787931"
---
# <a name="project-server-2013-architecture-and-programmability"></a><span data-ttu-id="fe962-104">Architecture de Project Server 2013 et programmabilité</span><span class="sxs-lookup"><span data-stu-id="fe962-104">Project Server 2013 architecture and programmability</span></span>

<span data-ttu-id="fe962-105">Les articles de cette section expliquent l’architecture globale de la solution Enterprise Project Management (EPM), qui combine Project Professional 2013, Project Server 2013, Project Web App et SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="fe962-105">The articles in this section describe the overall architecture of the Enterprise Project Management (EPM) solution, which combines Project Professional 2013, Project Server 2013, Project Web App, and SharePoint Server 2013.</span></span>
  
<span data-ttu-id="fe962-106">Project Server 2013 est générée avec le .NET Framework 4 et est la troisième version majeure de Project Server pour fournir une architecture à plusieurs couches de la valeur true.</span><span class="sxs-lookup"><span data-stu-id="fe962-106">Project Server 2013 is built with the .NET Framework 4 and is the third major release of Project Server to provide a true multitier architecture.</span></span> <span data-ttu-id="fe962-107">Pour l’accès nuage, Project Server 2013 implémente un modèle objet côté client (CSOM) et un service OData pour les rapports qui peut être utilisé dans les applications web, des applications mobiles et des applications Silverlight.</span><span class="sxs-lookup"><span data-stu-id="fe962-107">For cloud access, Project Server 2013 implements a client-side object model (CSOM) and an OData service for reporting that can be used in web applications, mobile applications, and Silverlight applications.</span></span> <span data-ttu-id="fe962-108">Pour les applications sur site, les clients peuvent utiliser les services de l’Interface de Project Server (PSI) ou le modèle CSOM.</span><span class="sxs-lookup"><span data-stu-id="fe962-108">For applications on-premises, clients can use either the CSOM or the Project Server Interface (PSI) services.</span></span> 
  
## <a name="introduction-to-project-server-architecture"></a><span data-ttu-id="fe962-109">Présentation de l’architecture de Project Server</span><span class="sxs-lookup"><span data-stu-id="fe962-109">Introduction to Project Server architecture</span></span>

<span data-ttu-id="fe962-110">Les rubriques de cette section décrivent l’architecture globale de la solution Enterprise Project Management (EPM), qui combine Project Professional 2013, Project Server 2013, Project Web App et SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="fe962-110">The topics in this section describe the overall architecture of the Enterprise Project Management (EPM) solution, which combines Project Professional 2013, Project Server 2013, Project Web App, and SharePoint Server 2013.</span></span>
  
<span data-ttu-id="fe962-111">Pour l’accès par programme à Project Server, vous devez utiliser le modèle CSOM ou services PSI avec l’interface de Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="fe962-111">For programmatic access to Project Server, you should use either the CSOM or the PSI services with the Windows Communication Foundation (WCF) interface.</span></span> <span data-ttu-id="fe962-112">L’interface ASMX du service web de la PSI est déconseillé dans Project Server 2013, mais il fonctionne toujours.</span><span class="sxs-lookup"><span data-stu-id="fe962-112">The ASMX web service interface of the PSI is deprecated in Project Server 2013, but still works.</span></span> <span data-ttu-id="fe962-113">La PSI permet un accès efficace à l’aide de jeux de données et vous pouvez créer des gestionnaires d’événements côté serveur.</span><span class="sxs-lookup"><span data-stu-id="fe962-113">The PSI enables efficient access by using datasets and you can create handlers for server-side events.</span></span> <span data-ttu-id="fe962-114">Le modèle CSOM lui-même utilise l’interface PSI pour accéder à la couche des objets métiers Project Server.</span><span class="sxs-lookup"><span data-stu-id="fe962-114">The CSOM itself uses the PSI to access the Project Server business object layer.</span></span> <span data-ttu-id="fe962-115">Au lieu de quatre bases de données Project Server, Project Server 2013 utilise une base de données dans la couche d’accès aux données.</span><span class="sxs-lookup"><span data-stu-id="fe962-115">Instead of four Project Server databases, Project Server 2013 uses a single database in the data access layer.</span></span>
  
<span data-ttu-id="fe962-116">Project Server 2013 intègre profondément SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="fe962-116">Project Server 2013 integrates deeply with SharePoint Server 2013.</span></span> <span data-ttu-id="fe962-117">Le Service d’Application Project peut être associé avec d’autres collections de sites SharePoint dans la batterie de serveurs.</span><span class="sxs-lookup"><span data-stu-id="fe962-117">The Project Application Service can be associated with other SharePoint site collections in the farm.</span></span> <span data-ttu-id="fe962-118">Project Server permettre exploiter et créer des rapports sur SharePoint, des listes de tâches dans la collection de sites et peuvent également prendre le contrôle où Project Server importe et gère les que listes de la tâche en tant que projets d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="fe962-118">Project Server can operate with and report on SharePoint task lists in the site collection, and can also get full control where Project Server imports and manages the task lists as enterprise projects.</span></span> <span data-ttu-id="fe962-119">Project Server utilise la version 4 de Windows Workflow Foundation (WF4) également et ajoute des activités de flux de travail pour les solutions de gestion de la demande.</span><span class="sxs-lookup"><span data-stu-id="fe962-119">Project Server also uses version 4 of the Windows Workflow Foundation (WF4) and adds workflow activities for Demand Management solutions.</span></span>
  
<span data-ttu-id="fe962-120">Pour une description des nouvelles fonctionnalités de Project 2013 offre aux développeurs et des fonctionnalités qui sont déconseillées, consultez [mises à jour pour les développeurs dans Project 2013](updates-for-developers-in-project-2013.md).</span><span class="sxs-lookup"><span data-stu-id="fe962-120">For a discussion of the many new features that Project 2013 provides for developers, and of the features that are deprecated, see [Updates for developers in Project 2013](updates-for-developers-in-project-2013.md).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="fe962-121">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="fe962-121">In this section</span></span>

<span data-ttu-id="fe962-122">[Architecture de Project Server 2013](project-server-2013-architecture.md) décrit les principaux composants de la plateforme de Project 2013, y compris les clients et les serveurs.</span><span class="sxs-lookup"><span data-stu-id="fe962-122">[Project Server 2013 architecture](project-server-2013-architecture.md) describes the major parts of the Project 2013 platform, including the clients and servers.</span></span> 
  
<span data-ttu-id="fe962-123">[Programmabilité de Project Server](project-server-programmability.md) présente les fonctionnalités d’extensibilité principale de Project Server 2013, la personnalisation de Project Web App et mise à niveau des applications qui sont créées pour les versions antérieures de Project Server.</span><span class="sxs-lookup"><span data-stu-id="fe962-123">[Project Server programmability](project-server-programmability.md) discusses the main extensibility features of Project Server 2013, customization of Project Web App, and upgrading applications that are built for previous Project Server versions.</span></span> 
  
<span data-ttu-id="fe962-124">[Ce que la PSI fait et ne fait pas](what-the-psi-does-and-does-not-do.md) décrit des scénarios où la PSI peut être utilisée et répertorie les opérations PSI ne peut pas faire.</span><span class="sxs-lookup"><span data-stu-id="fe962-124">[What the PSI does and does not do](what-the-psi-does-and-does-not-do.md) describes scenarios where the PSI can be used and lists things that the PSI cannot do.</span></span> 
  
<span data-ttu-id="fe962-125">[Ce que le modèle et ne](what-the-csom-does-and-does-not-do.md) décrit des scénarios où le modèle peut être utilisé et répertorie les opérations CSOM ne peut pas faire.</span><span class="sxs-lookup"><span data-stu-id="fe962-125">[What the CSOM does and does not do](what-the-csom-does-and-does-not-do.md) describes scenarios where the CSOM can be used and lists things that the CSOM cannot do.</span></span> 
  
### <a name="topics-not-covered"></a><span data-ttu-id="fe962-126">Rubriques ne pas</span><span class="sxs-lookup"><span data-stu-id="fe962-126">Topics not covered</span></span>

<span data-ttu-id="fe962-127">Les articles de la section *Architecture et programmabilité* ne document pas les fonctionnalités des clients de bureau de projet (Project Standard 2013 et Project Professional 2013) Project Web App.</span><span class="sxs-lookup"><span data-stu-id="fe962-127">The articles in the  *Architecture and programmability*  section do not document features of the Project desktop clients (Project Standard 2013 and Project Professional 2013) or Project Web App.</span></span> 
  
<span data-ttu-id="fe962-128">Visual Basic pour l’aide d’Applications (VBA) est disponible dans Visual Basic editor dans Project Standard et Project Professional.</span><span class="sxs-lookup"><span data-stu-id="fe962-128">Visual Basic for Applications (VBA) help is available in the Visual Basic editor within Project Standard and Project Professional.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fe962-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe962-129">See also</span></span>
<span data-ttu-id="fe962-130"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="fe962-130"></span></span>

- [<span data-ttu-id="fe962-131">Mises à jour pour les développeurs dans Project 2013</span><span class="sxs-lookup"><span data-stu-id="fe962-131">Updates for developers in Project 2013</span></span>](updates-for-developers-in-project-2013.md)
    
- [<span data-ttu-id="fe962-132">Prise en main développement flux de travail Project Server</span><span class="sxs-lookup"><span data-stu-id="fe962-132">Getting started developing Project Server workflows</span></span>](getting-started-developing-project-server-workflows.md)
    

