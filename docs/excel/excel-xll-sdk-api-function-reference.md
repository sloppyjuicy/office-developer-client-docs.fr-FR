---
title: Référence de la fonction API SDK XLL Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- référence des fonctions d’API [excel 2007], fonctions [Excel 2007], référence [Excel 2007], du Kit de développement logiciel Excel 2007 XLL, référence
localization_priority: Normal
api_type:
- COM
ms.assetid: 2f6df879-7546-4ac0-a4e3-6b009aee9463
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 2bb0a57ebcae618c8e921135b2bd4c50e8adf751
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782120"
---
# <a name="excel-xll-sdk-api-function-reference"></a><span data-ttu-id="545a9-104">Référence de la fonction API SDK XLL Excel</span><span class="sxs-lookup"><span data-stu-id="545a9-104">Excel XLL SDK API Function Reference</span></span>

<span data-ttu-id="545a9-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="545a9-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="545a9-106">Le SDK XLL Microsoft Excel 2013 contient des fichiers sources pour une bibliothèque Framework qui est conçu pour accélérer l’écriture de XLL et deux exemples de projets, exemple et générique.</span><span class="sxs-lookup"><span data-stu-id="545a9-106">The Microsoft Excel 2013 XLL SDK contains source files for a Framework library that is designed to speed up the writing of XLLs, and two sample projects, Example and Generic.</span></span> 
  
<span data-ttu-id="545a9-107">Cette section fournit une référence de fonction pour les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="545a9-107">This section provides a function reference for the following:</span></span>
  
- <span data-ttu-id="545a9-108">Rappels Excel la XLL peut appeler.</span><span class="sxs-lookup"><span data-stu-id="545a9-108">Excel callbacks that the XLL can call.</span></span>
    
- <span data-ttu-id="545a9-109">Rappels XLL Microsoft Excel recherche.</span><span class="sxs-lookup"><span data-stu-id="545a9-109">XLL callbacks that Microsoft Excel looks for.</span></span>
    
- <span data-ttu-id="545a9-110">Fonctions clés dans les projets exemple et framework.</span><span class="sxs-lookup"><span data-stu-id="545a9-110">Key functions in the sample and framework projects.</span></span>
    
## <a name="sample-projects"></a><span data-ttu-id="545a9-111">Exemples de projets</span><span class="sxs-lookup"><span data-stu-id="545a9-111">Sample projects</span></span>

<span data-ttu-id="545a9-112">Le Kit de développement logiciel XLL Excel 2013 fournit des fichiers source et fichiers de projet Microsoft Visual Studio pour les exemples de projet suivants :</span><span class="sxs-lookup"><span data-stu-id="545a9-112">The Excel 2013 XLL SDK provides source files and Microsoft Visual Studio project files for the following sample projects:</span></span>
  
- <span data-ttu-id="545a9-113">Le projet **Framework** (`SAMPLES\FRAMEWRK\`) contient un projet qui peut être créé dans une bibliothèque, FRAMEWRK.lib, qui peut ensuite être lié dans d’autres projets XLL.</span><span class="sxs-lookup"><span data-stu-id="545a9-113">The **Framework** project (`SAMPLES\FRAMEWRK\`) contains a project that can be built to a library, FRAMEWRK.lib, which can then be linked into other XLL projects.</span></span> <span data-ttu-id="545a9-114">La bibliothèque contient plusieurs fonctions et les outils qui facilitent l’écriture de XLL plus faciles.</span><span class="sxs-lookup"><span data-stu-id="545a9-114">The library contains many functions and tools that make writing XLLs easier.</span></span> <span data-ttu-id="545a9-115">Cette bibliothèque est utilisée dans les deux autres projets en association avec le fichier d’en-tête FRAMEWRK.h.</span><span class="sxs-lookup"><span data-stu-id="545a9-115">This library is used in both of the other projects in conjunction with the header file FRAMEWRK.h.</span></span>
    
- <span data-ttu-id="545a9-116">**L’exemple** de projet (`SAMPLES\EXAMPLE\`) contient un projet pouvant être créées pour un XLL, EXAMPLE.xll.</span><span class="sxs-lookup"><span data-stu-id="545a9-116">The **Example** project (`SAMPLES\EXAMPLE\`) contains a project that can be built to an XLL, EXAMPLE.xll.</span></span> <span data-ttu-id="545a9-117">La ressource XLL contient de nombreux exemples de l’utilisation de la bibliothèque Framework et exemples d’implémentation des fonctions telles que **xlAutoOpen**interface complément XLL.</span><span class="sxs-lookup"><span data-stu-id="545a9-117">The XLL contains many examples of the use of the Framework library, and example implementations of the XLL add-in interface functions such as **xlAutoOpen**.</span></span>
    
- <span data-ttu-id="545a9-118">Le projet **générique** (`SAMPLES\GENERIC\`) contient un projet pouvant être créées pour un XLL, GENERIC.xll.</span><span class="sxs-lookup"><span data-stu-id="545a9-118">The **Generic** project (`SAMPLES\GENERIC\`) contains a project that can be built to an XLL, GENERIC.xll.</span></span> <span data-ttu-id="545a9-119">La ressource XLL illustre plusieurs exemples de fonctions et commandes et est un bon point de départ pour l’écriture de votre propre XLL.</span><span class="sxs-lookup"><span data-stu-id="545a9-119">The XLL demonstrates several example functions and commands and is a good starting point for writing your own XLLs.</span></span>
    
## <a name="in-this-section"></a><span data-ttu-id="545a9-120">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="545a9-120">In this section</span></span>

- [<span data-ttu-id="545a9-121">Gestionnaire de compléments et les fonctions de l’Interface XLL</span><span class="sxs-lookup"><span data-stu-id="545a9-121">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)
  
- [<span data-ttu-id="545a9-122">Les fonctions de rappel de l'API C Excel4, Excel12</span><span class="sxs-lookup"><span data-stu-id="545a9-122">C API Callback Functions Excel4, Excel12</span></span>](c-api-callback-functions-excel4-excel12.md)
  
- [<span data-ttu-id="545a9-123">Fonctions XLM API C essentielles et utiles</span><span class="sxs-lookup"><span data-stu-id="545a9-123">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)
  
- [<span data-ttu-id="545a9-124">Fonctions de l’API C qui peuvent être appelées uniquement à partir d’une DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="545a9-124">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
- [<span data-ttu-id="545a9-125">Fonctions de la bibliothèque Framework</span><span class="sxs-lookup"><span data-stu-id="545a9-125">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)
  
- [<span data-ttu-id="545a9-126">Fonctions de la DLL générique</span><span class="sxs-lookup"><span data-stu-id="545a9-126">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)
  
- [<span data-ttu-id="545a9-127">Fonctions du connecteur de Cluster Excel</span><span class="sxs-lookup"><span data-stu-id="545a9-127">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)
  
## <a name="see-also"></a><span data-ttu-id="545a9-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="545a9-128">See also</span></span>

- [<span data-ttu-id="545a9-129">Programmation avec l�API�C dans Excel</span><span class="sxs-lookup"><span data-stu-id="545a9-129">Programming with the C API in Excel</span></span>](programming-with-the-c-api-in-excel.md)
  
- [<span data-ttu-id="545a9-130">D�veloppement de XLL de Excel 2013</span><span class="sxs-lookup"><span data-stu-id="545a9-130">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

