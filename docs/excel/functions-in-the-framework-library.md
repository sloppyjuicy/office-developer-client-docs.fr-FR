---
title: Fonctions dans la bibliothèque d’infrastructure
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- framework library functions [excel 2007],functions [Excel 2007], Framework library
localization_priority: Normal
ms.assetid: 7d9a13fd-9a4c-423e-bb08-4a5be57c7905
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4eeb9e5db09592e98e9afb763efaa6be18eb2f7e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417545"
---
# <a name="functions-in-the-framework-library"></a><span data-ttu-id="92d16-104">Fonctions dans la bibliothèque d’infrastructure</span><span class="sxs-lookup"><span data-stu-id="92d16-104">Functions in the Framework Library</span></span>

<span data-ttu-id="92d16-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="92d16-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="92d16-106">La bibliothèque Framework a été créée pour faciliter l’écriture de XL.</span><span class="sxs-lookup"><span data-stu-id="92d16-106">The Framework Library was created to help make writing XLLs easier.</span></span> <span data-ttu-id="92d16-107">Il inclut des fonctions simples pour la gestion de la mémoire **XLOPER** XLOPER12, la création temporaire de XLOPER XLOPER12 , l’appel robuste des fonctions de rappel /   Microsoft Excel  /  (**Excel4**, **Excel4v**, \*\* Excel12 \*\*, \*\* Excel12v \*\*) et l’impression de chaînes de débogage sur un terminal attaché.</span><span class="sxs-lookup"><span data-stu-id="92d16-107">It includes simple functions for managing **XLOPER**/ **XLOPER12** memory, creating temporary **XLOPER**/ **XLOPER12**, robustly calling the Microsoft Excel callback functions (**Excel4**, **Excel4v**, \*\* Excel12 \*\*, \*\* Excel12v \*\*) and printing debugging strings on an attached terminal.</span></span>
  
<span data-ttu-id="92d16-108">Les fonctions incluses dans cette bibliothèque facilitent la simplification d’un élément de code qui ressemble à ce qui suit.</span><span class="sxs-lookup"><span data-stu-id="92d16-108">The functions included in this library help simplify a piece of code that looks like the following.</span></span>
  
```cs
XLOPER12 xMissing, xBool;
xMissing.xltype = xltypeMissing;
xBool.xltype = xltypeBool;
xBool.val.xbool = 0;
Excel12(xlcDisplay, 0, 2, (LPXLOPER12) &xMissing, (LPXLOPER12) &xBool);
```

<span data-ttu-id="92d16-109">Le code simplifié ressemble à l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="92d16-109">The simplified code looks like the following example.</span></span>
  
```cs
Excel12f(xlcDisplay, 0, 2, TempMissing12(), TempBool12(0));
```

<span data-ttu-id="92d16-110">Les fonctions suivantes sont incluses dans la bibliothèque Framework :</span><span class="sxs-lookup"><span data-stu-id="92d16-110">The following functions are included in the Framework library:</span></span>
  
||
|:-----|
|[<span data-ttu-id="92d16-111">debugPrintf</span><span class="sxs-lookup"><span data-stu-id="92d16-111">debugPrintf</span></span>](debugprintf.md) <br/> |
|<span data-ttu-id="92d16-112">**GetTempMemory**</span><span class="sxs-lookup"><span data-stu-id="92d16-112">**GetTempMemory**</span></span> <br/> |
|<span data-ttu-id="92d16-113">**FreeAllTempMemory**</span><span class="sxs-lookup"><span data-stu-id="92d16-113">**FreeAllTempMemory**</span></span> <br/> |
|[<span data-ttu-id="92d16-114">InitFramework</span><span class="sxs-lookup"><span data-stu-id="92d16-114">InitFramework</span></span>](initframework.md) <br/> |
|[<span data-ttu-id="92d16-115">QuitFramework</span><span class="sxs-lookup"><span data-stu-id="92d16-115">QuitFramework</span></span>](quitframework.md) <br/> |
   
|<span data-ttu-id="92d16-116">**Fonctions utilisées avec xlOPERs**</span><span class="sxs-lookup"><span data-stu-id="92d16-116">**Functions Used with XLOPERs**</span></span>|<span data-ttu-id="92d16-117">**Fonctions utilisées avec XLOPER12s**</span><span class="sxs-lookup"><span data-stu-id="92d16-117">**Functions Used with XLOPER12s**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="92d16-118">Excel</span><span class="sxs-lookup"><span data-stu-id="92d16-118">Excel</span></span>](excel-excel12f.md) <br/> |[<span data-ttu-id="92d16-119">Excel12f</span><span class="sxs-lookup"><span data-stu-id="92d16-119">Excel12f</span></span>](excel-excel12f.md) <br/> |
|[<span data-ttu-id="92d16-120">TempNum</span><span class="sxs-lookup"><span data-stu-id="92d16-120">TempNum</span></span>](tempnum-tempnum12.md) <br/> |[<span data-ttu-id="92d16-121">TempNum12</span><span class="sxs-lookup"><span data-stu-id="92d16-121">TempNum12</span></span>](tempnum-tempnum12.md) <br/> |
|[<span data-ttu-id="92d16-122">TempStr</span><span class="sxs-lookup"><span data-stu-id="92d16-122">TempStr</span></span>](tempstr.md) <br/> |[<span data-ttu-id="92d16-123">TempStr12</span><span class="sxs-lookup"><span data-stu-id="92d16-123">TempStr12</span></span>](tempstrconst-tempstr12.md) <br/> |
|[<span data-ttu-id="92d16-124">TempStrConst</span><span class="sxs-lookup"><span data-stu-id="92d16-124">TempStrConst</span></span>](tempstrconst-tempstr12.md) <br/> |[<span data-ttu-id="92d16-125">TempStr12Const</span><span class="sxs-lookup"><span data-stu-id="92d16-125">TempStr12Const</span></span>](tempstrconst-tempstr12.md) <br/> |
|[<span data-ttu-id="92d16-126">TempBool</span><span class="sxs-lookup"><span data-stu-id="92d16-126">TempBool</span></span>](tempbool-tempbool12.md) <br/> |[<span data-ttu-id="92d16-127">TempBool12</span><span class="sxs-lookup"><span data-stu-id="92d16-127">TempBool12</span></span>](tempbool-tempbool12.md) <br/> |
|[<span data-ttu-id="92d16-128">TempInt</span><span class="sxs-lookup"><span data-stu-id="92d16-128">TempInt</span></span>](tempint-tempint12.md) <br/> |[<span data-ttu-id="92d16-129">TempInt12</span><span class="sxs-lookup"><span data-stu-id="92d16-129">TempInt12</span></span>](tempint-tempint12.md) <br/> |
|[<span data-ttu-id="92d16-130">TempErr</span><span class="sxs-lookup"><span data-stu-id="92d16-130">TempErr</span></span>](temperr-temperr12.md) <br/> |[<span data-ttu-id="92d16-131">TempErr12</span><span class="sxs-lookup"><span data-stu-id="92d16-131">TempErr12</span></span>](temperr-temperr12.md) <br/> |
|[<span data-ttu-id="92d16-132">TempActiveRef</span><span class="sxs-lookup"><span data-stu-id="92d16-132">TempActiveRef</span></span>](tempactiveref-tempactiveref12.md) <br/> |[<span data-ttu-id="92d16-133">TempActiveRef12</span><span class="sxs-lookup"><span data-stu-id="92d16-133">TempActiveRef12</span></span>](tempactiveref-tempactiveref12.md) <br/> |
|[<span data-ttu-id="92d16-134">TempActiveCell</span><span class="sxs-lookup"><span data-stu-id="92d16-134">TempActiveCell</span></span>](tempactivecell-tempactivecell12.md) <br/> |[<span data-ttu-id="92d16-135">TempActiveCell12</span><span class="sxs-lookup"><span data-stu-id="92d16-135">TempActiveCell12</span></span>](tempactivecell-tempactivecell12.md) <br/> |
|[<span data-ttu-id="92d16-136">TempActiveRow</span><span class="sxs-lookup"><span data-stu-id="92d16-136">TempActiveRow</span></span>](tempactiverow-tempactiverow12.md) <br/> |[<span data-ttu-id="92d16-137">TempActiveRow12</span><span class="sxs-lookup"><span data-stu-id="92d16-137">TempActiveRow12</span></span>](tempactiverow-tempactiverow12.md) <br/> |
|[<span data-ttu-id="92d16-138">TempActiveColumn</span><span class="sxs-lookup"><span data-stu-id="92d16-138">TempActiveColumn</span></span>](tempactivecolumn-tempactivecolumn12.md) <br/> |[<span data-ttu-id="92d16-139">TempActiveColumn12</span><span class="sxs-lookup"><span data-stu-id="92d16-139">TempActiveColumn12</span></span>](tempactivecolumn-tempactivecolumn12.md) <br/> |
|[<span data-ttu-id="92d16-140">TempMissing</span><span class="sxs-lookup"><span data-stu-id="92d16-140">TempMissing</span></span>](tempmissing-tempmissing12.md) <br/> |[<span data-ttu-id="92d16-141">TempMissing12</span><span class="sxs-lookup"><span data-stu-id="92d16-141">TempMissing12</span></span>](tempmissing-tempmissing12.md) <br/> |
   
<span data-ttu-id="92d16-142">L’utilisation de ces fonctions réduit le temps nécessaire à l’écriture d’une DLL ou d’une XLL.</span><span class="sxs-lookup"><span data-stu-id="92d16-142">Use of these functions shortens the amount of time required to write a DLL or XLL.</span></span> <span data-ttu-id="92d16-143">Le démarrage du développement à partir de l’exemple d’application GENERIC raccourcit également le temps de développement.</span><span class="sxs-lookup"><span data-stu-id="92d16-143">Starting development from the sample application GENERIC also shortens development time.</span></span> <span data-ttu-id="92d16-144">Utilisez GENERIC. C en tant que modèle pour vous aider à configurer l’infrastructure d’une XLL, puis à remplacer le code existant par le vôtre.</span><span class="sxs-lookup"><span data-stu-id="92d16-144">Use GENERIC.C as a template to help set up the framework of an XLL, and then replace the existing code with your own.</span></span>
  
<span data-ttu-id="92d16-145">Les fonctions **XLOPER** /  **XLOPER12** temporaires créent des valeurs  /  **XLOPER XLOPER12** à l’aide de la mémoire d’un tas local géré par la bibliothèque Framework.</span><span class="sxs-lookup"><span data-stu-id="92d16-145">The temporary **XLOPER**/ **XLOPER12** functions create **XLOPER**/ **XLOPER12** values by using memory from a local heap managed by the Framework library.</span></span> <span data-ttu-id="92d16-146">Les **valeurs XLOPER** XLOPER12 restent valides jusqu’à ce que vous appeliez la fonction /   **FreeAllTempMemory** ou l’une des fonctions **Excel** ou **Excel12f.**</span><span class="sxs-lookup"><span data-stu-id="92d16-146">The **XLOPER**/ **XLOPER12** values remain valid until you call the **FreeAllTempMemory** function or either of the **Excel** or **Excel12f** functions.</span></span> <span data-ttu-id="92d16-147">(Les **fonctions Excel** **excel12f** libèrent toute la mémoire temporaire avant de revenir.)</span><span class="sxs-lookup"><span data-stu-id="92d16-147">(The **Excel** and **Excel12f** functions free all temporary memory before returning.)</span></span> 
  
<span data-ttu-id="92d16-148">Pour utiliser les fonctions de la bibliothèque Framework, vous devez inclure FRAMEWRK. Fichier H dans votre code C et ajoutez frameWRK. C ou FRMWRK32. Fichiers LIB dans votre projet de code.</span><span class="sxs-lookup"><span data-stu-id="92d16-148">To use the Framework library functions, you must include the FRAMEWRK.H file in your C code and add the FRAMEWRK.C or FRMWRK32.LIB files to your code project.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="92d16-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92d16-149">See also</span></span>

- [<span data-ttu-id="92d16-150">Référence des fonctions XLL SDK API Excel 2013</span><span class="sxs-lookup"><span data-stu-id="92d16-150">Excel XLL SDK API Function Reference</span></span>](excel-xll-sdk-api-function-reference.md)

