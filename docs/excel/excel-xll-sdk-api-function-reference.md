---
title: Référence des fonctions XLL SDK API Excel 2013
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Référence des fonctions API [Excel 2007], fonctions [Excel 2007], référence [Excel 2007] Kit de développement logiciel Excel 2007 XLL, référence
api_type:
- COM
ms.assetid: 2f6df879-7546-4ac0-a4e3-6b009aee9463
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: e116021a3dc24de7decbe0dad76cc762cd66d032
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304122"
---
# <a name="excel-xll-sdk-api-function-reference"></a><span data-ttu-id="f499f-104">Référence des fonctions XLL SDK API Excel 2013</span><span class="sxs-lookup"><span data-stu-id="f499f-104">Excel XLL SDK API Function Reference</span></span>

<span data-ttu-id="f499f-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f499f-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="f499f-106">Le kit de développement XLL Microsoft Excel 2013 contient les fichiers sources d’une bibliothèque Framework conçue pour accélérer la rédaction de fichiers XLL, ainsi que deux exemples de projets : Example et Generic.</span><span class="sxs-lookup"><span data-stu-id="f499f-106">The Microsoft Excel 2013 XLL SDK contains source files for a Framework library that is designed to speed up the writing of XLLs, and two sample projects, Example and Generic.</span></span> 
  
<span data-ttu-id="f499f-107">Cette section fournit une référence des fonctions pour les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="f499f-107">This section provides a function reference for the following:</span></span>
  
- <span data-ttu-id="f499f-108">Rappels Excel que XLL peut appeler.</span><span class="sxs-lookup"><span data-stu-id="f499f-108">Excel callbacks that the XLL can call.</span></span>
    
- <span data-ttu-id="f499f-109">Rappels XLL que Microsoft Excel peut rechercher.</span><span class="sxs-lookup"><span data-stu-id="f499f-109">XLL callbacks that Microsoft Excel looks for.</span></span>
    
- <span data-ttu-id="f499f-110">Fonctions principales dans les projets d’exemple et de cadre.</span><span class="sxs-lookup"><span data-stu-id="f499f-110">Key functions in the sample and framework projects.</span></span>
    
## <a name="sample-projects"></a><span data-ttu-id="f499f-111">Exemples de projets</span><span class="sxs-lookup"><span data-stu-id="f499f-111">Sample projects</span></span>

<span data-ttu-id="f499f-112">Le kit de développement XLL Excel 2013 fournit des fichiers sources et des fichiers de projet Microsoft Visual Studio pour les projets d’exemple suivants :</span><span class="sxs-lookup"><span data-stu-id="f499f-112">The Excel 2013 XLL SDK provides source files and Microsoft Visual Studio project files for the following sample projects:</span></span>
  
- <span data-ttu-id="f499f-113">Le projet **Framework** (`SAMPLES\FRAMEWRK\`) contient un projet qui peut être intégré dans une bibliothèque, FRAMEWRK.lib, qui peut ensuite être lié à d’autres projets XLL.</span><span class="sxs-lookup"><span data-stu-id="f499f-113">The **Framework** project (`SAMPLES\FRAMEWRK\`) contains a project that can be built to a library, FRAMEWRK.lib, which can then be linked into other XLL projects.</span></span> <span data-ttu-id="f499f-114">La bibliothèque contient de nombreuses fonctions et outils qui simplifient la rédaction de fichiers XLL.</span><span class="sxs-lookup"><span data-stu-id="f499f-114">The library contains many functions and tools that make writing XLLs easier.</span></span> <span data-ttu-id="f499f-115">Cette bibliothèque est utilisée dans les deux autres projets conjointement avec le fichier d’en-tête FRAMEWRK.h.</span><span class="sxs-lookup"><span data-stu-id="f499f-115">This library is used in both of the other projects in conjunction with the header file FRAMEWRK.h.</span></span>
    
- <span data-ttu-id="f499f-116">Le projet **Example** (`SAMPLES\EXAMPLE\`) contient un projet qui peut être intégré à un fichier XLL, EXAMPLE.xll.</span><span class="sxs-lookup"><span data-stu-id="f499f-116">The **Example** project (`SAMPLES\EXAMPLE\`) contains a project that can be built to an XLL, EXAMPLE.xll.</span></span> <span data-ttu-id="f499f-117">Le fichier XLL contient de nombreux exemples d’utilisation de la bibliothèque Framework, ainsi que des exemples d’implémentation des fonctions d’interface du complément XLL telles que **xlAutoOpen**.</span><span class="sxs-lookup"><span data-stu-id="f499f-117">The XLL contains many examples of the use of the Framework library, and example implementations of the XLL add-in interface functions such as **xlAutoOpen**.</span></span>
    
- <span data-ttu-id="f499f-118">Le projet **Generic** (`SAMPLES\GENERIC\`) contient un projet qui peut être intégré à un fichier XLL, GENERIC.xll.</span><span class="sxs-lookup"><span data-stu-id="f499f-118">The **Generic** project (`SAMPLES\GENERIC\`) contains a project that can be built to an XLL, GENERIC.xll.</span></span> <span data-ttu-id="f499f-119">Le fichier XLL illustre plusieurs exemples de fonction et de commande, et constitue un bon point de départ pour la rédaction de vos propres fichiers XLL.</span><span class="sxs-lookup"><span data-stu-id="f499f-119">The XLL demonstrates several example functions and commands and is a good starting point for writing your own XLLs.</span></span>
    
## <a name="in-this-section"></a><span data-ttu-id="f499f-120">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="f499f-120">In this section</span></span>

- [<span data-ttu-id="f499f-121">Fonctions du Gestionnaire de compléments et de l’interface XLL</span><span class="sxs-lookup"><span data-stu-id="f499f-121">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)
  
- [<span data-ttu-id="f499f-122">Fonctions de rappel de l’API C Excel4, Excel12</span><span class="sxs-lookup"><span data-stu-id="f499f-122">C API Callback Functions Excel4, Excel12</span></span>](c-api-callback-functions-excel4-excel12.md)
  
- [<span data-ttu-id="f499f-123">Fonctions XLM essentielles et utiles de l’API C</span><span class="sxs-lookup"><span data-stu-id="f499f-123">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)
  
- [<span data-ttu-id="f499f-124">Fonctions de l’API C à appeler à partir d’un fichier DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="f499f-124">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
- [<span data-ttu-id="f499f-125">Fonctions de la bibliothèque Framework</span><span class="sxs-lookup"><span data-stu-id="f499f-125">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)
  
- [<span data-ttu-id="f499f-126">Fonctions dans le fichier DLL générique</span><span class="sxs-lookup"><span data-stu-id="f499f-126">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)
  
- [<span data-ttu-id="f499f-127">Fonctions du connecteur de cluster Excel</span><span class="sxs-lookup"><span data-stu-id="f499f-127">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)
  
## <a name="see-also"></a><span data-ttu-id="f499f-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f499f-128">See also</span></span>

- [<span data-ttu-id="f499f-129">Programmation avec l�API C dans Excel</span><span class="sxs-lookup"><span data-stu-id="f499f-129">Programming with the C API in Excel</span></span>](programming-with-the-c-api-in-excel.md)
  
- [<span data-ttu-id="f499f-130">Développement de XLL de Excel 2013</span><span class="sxs-lookup"><span data-stu-id="f499f-130">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

