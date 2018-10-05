---
title: Bienvenue dans le Kit de développement logiciel (SDK) Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- excel 2007 xll software development kit,add-ins [Excel 2007]
localization_priority: Normal
ms.assetid: abfc9d76-6f22-49b9-ba45-eb7a54b082e0
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 492b8097c681ec072d2ec3ca26a9a2bfeba054ff
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392360"
---
# <a name="welcome-to-the-excel-software-development-kit"></a><span data-ttu-id="6bf22-104">Bienvenue dans le Kit de développement logiciel (SDK) Excel</span><span class="sxs-lookup"><span data-stu-id="6bf22-104">Welcome to the Excel Software Development Kit</span></span>

 <span data-ttu-id="6bf22-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6bf22-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="6bf22-p101">Bienvenue dans la documentation du kit de développement logiciel (SDK) XLL Excel 2013. Cette référence contient des vues d’ensemble conceptuelles, des tâches de programmation et des exemples pour vous aider à développer des XLL Microsoft Excel 2013.</span><span class="sxs-lookup"><span data-stu-id="6bf22-p101">Welcome to the Excel 2013 XLL Software Development Kit (SDK) documentation. This reference contains conceptual overviews, programming tasks, and samples to help you develop Microsoft Excel 2013 XLLs.</span></span>
  
<span data-ttu-id="6bf22-108">Révision : novembre 2012</span><span class="sxs-lookup"><span data-stu-id="6bf22-108">Revised: November 2012</span></span>
  
<span data-ttu-id="6bf22-109">Téléchargez le [SDK XLL Excel 2013](https://go.microsoft.com/fwlink/?LinkID=251082&amp;clcid=0x409).</span><span class="sxs-lookup"><span data-stu-id="6bf22-109">Download the [Excel 2013 XLL SDK](https://go.microsoft.com/fwlink/?LinkID=251082&amp;clcid=0x409).</span></span>
  
<span data-ttu-id="6bf22-110">Le SDK XLL Excel 2013 comprend les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="6bf22-110">The Excel 2013 XLL SDK includes the following:</span></span>
  
- <span data-ttu-id="6bf22-111">**Interface de programmation d’application (API) C** : inclut les fichiers d’en-tête et sources qui permettent aux DLL d’accéder à la fonctionnalité Excel 2013, ainsi qu’une description de l’interface dont doit disposer une DLL pour utiliser le Gestionnaire de compléments Excel.</span><span class="sxs-lookup"><span data-stu-id="6bf22-111">**C application programming interface (API)**—Includes header and source files that enable DLLs to access Excel 2013 functionality, and a description of the interface that a DLL should expose to work with the Excel Add-in Manager.</span></span>
    
- <span data-ttu-id="6bf22-p102">**Projets Microsoft Visual Studio** : incluent le code source C/C++ et montrent comment utiliser l’API C. Ces exemples de projets servent de point de départ à votre développement personnel de compléments.</span><span class="sxs-lookup"><span data-stu-id="6bf22-p102">**Microsoft Visual Studio projects**—Includes C/C++ source code and shows how to use the C API. These sample projects provide examples and they serve as a starting point for your own add-in development.</span></span>
    
<span data-ttu-id="6bf22-114">La documentation du SDK contient les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="6bf22-114">The SDK documentation contains the following sections:</span></span>
  
- [<span data-ttu-id="6bf22-115">Mise en route avec le Kit de développement logiciel XLL Excel 2013</span><span class="sxs-lookup"><span data-stu-id="6bf22-115">Getting Started with the Excel XLL SDK</span></span>](getting-started-with-the-excel-xll-sdk.md)
    
- [<span data-ttu-id="6bf22-116">Développement de XLL de Excel 2013</span><span class="sxs-lookup"><span data-stu-id="6bf22-116">Developing Excel XLLs</span></span>](developing-excel-xlls.md)
    
- [<span data-ttu-id="6bf22-117">Développement de connecteurs de Cluster Excel 2013</span><span class="sxs-lookup"><span data-stu-id="6bf22-117">Developing Excel Cluster Connectors</span></span>](developing-excel-cluster-connectors.md)
    
- [<span data-ttu-id="6bf22-118">Référence des fonctions XLL SDK API Excel 2013</span><span class="sxs-lookup"><span data-stu-id="6bf22-118">Excel XLL SDK API Function Reference</span></span>](excel-xll-sdk-api-function-reference.md)
    
## <a name="functionality-not-covered"></a><span data-ttu-id="6bf22-119">Fonction non traitée</span><span class="sxs-lookup"><span data-stu-id="6bf22-119">Functionality Not Covered</span></span>

<span data-ttu-id="6bf22-120">Les sujets suivants ne sont pas traités :</span><span class="sxs-lookup"><span data-stu-id="6bf22-120">The following subjects are not covered:</span></span>
  
- <span data-ttu-id="6bf22-121">Développement de fonctions et commandes définies par l’utilisateur dans les feuilles de calcul macro (XLM) Excel.</span><span class="sxs-lookup"><span data-stu-id="6bf22-121">Developing user-defined functions and commands in Excel macro (XLM) sheets.</span></span>
    
- <span data-ttu-id="6bf22-122">Création de fonctions définies par l’utilisateur dans des DLL qui contrôlent le flux d’exécution d’une macro XLM.</span><span class="sxs-lookup"><span data-stu-id="6bf22-122">Creating user-defined functions in DLLs that control the flow of execution of an XLM macro.</span></span>
    
    <span data-ttu-id="6bf22-123">Ces fonctions œuvrent en renvoyant un type de données de contrôle de flux spécial, qui n’est pas non plus décrit dans cette documentation.</span><span class="sxs-lookup"><span data-stu-id="6bf22-123">Such functions work by returning a special flow control data type, which is also not described in this documentation.</span></span>
    
## <a name="related-links"></a><span data-ttu-id="6bf22-124">Liens connexes</span><span class="sxs-lookup"><span data-stu-id="6bf22-124">Related Links</span></span>

[<span data-ttu-id="6bf22-125">Centre pour développeurs Excel</span><span class="sxs-lookup"><span data-stu-id="6bf22-125">Excel Developer Center</span></span>](https://msdn.microsoft.com/office/aa905411.aspx)
  
[<span data-ttu-id="6bf22-126">Centre pour développeurs Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="6bf22-126">Microsoft Office Developer Center</span></span>](https://msdn.microsoft.com/office/default.aspx)
  
[<span data-ttu-id="6bf22-127">SDK Excel 2010 : kit de développement logiciel XLL Excel 2010</span><span class="sxs-lookup"><span data-stu-id="6bf22-127">Excel 2010 SDK: Excel 2010 XLL Software Development Kit</span></span>](https://go.microsoft.com/fwlink/?LinkID=186435&amp;clcid=0x409)
  

