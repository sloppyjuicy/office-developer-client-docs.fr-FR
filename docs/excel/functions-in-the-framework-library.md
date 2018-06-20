---
title: Fonctions de la bibliothèque Framework
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- fonctions de la bibliothèque Framework [excel 2007], fonctions [Excel 2007], bibliothèque Framework
localization_priority: Normal
ms.assetid: 7d9a13fd-9a4c-423e-bb08-4a5be57c7905
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 1d3878e376f95be3b277f1bb1a59545eb0a631ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782139"
---
# <a name="functions-in-the-framework-library"></a><span data-ttu-id="8f68d-104">Fonctions de la bibliothèque Framework</span><span class="sxs-lookup"><span data-stu-id="8f68d-104">Functions in the Framework Library</span></span>

<span data-ttu-id="8f68d-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8f68d-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="8f68d-106">La bibliothèque Framework a été créée pour faciliter l’écriture de XLL plus faciles.</span><span class="sxs-lookup"><span data-stu-id="8f68d-106">The Framework Library was created to help make writing XLLs easier.</span></span> <span data-ttu-id="8f68d-107">Il inclut des fonctions de gestion **XLOPER**simples/ mémoire**XLOPER12** , création temporaire **XLOPER**/ **XLOPER12**, stricte appeler les fonctions de rappel de Microsoft Excel (**Excel 4**, **Excel4v** ** Excel12 **, ** Excel12v **) et l’impression de débogage des chaînes dans un terminal attaché.</span><span class="sxs-lookup"><span data-stu-id="8f68d-107">It includes simple functions for managing **XLOPER**/ **XLOPER12** memory, creating temporary **XLOPER**/ **XLOPER12**, robustly calling the Microsoft Excel callback functions (**Excel4**, **Excel4v**, ** Excel12 **, ** Excel12v **) and printing debugging strings on an attached terminal.</span></span>
  
<span data-ttu-id="8f68d-108">Les fonctions incluses dans cette bibliothèque de simplifier un morceau de code qui se présente comme suit.</span><span class="sxs-lookup"><span data-stu-id="8f68d-108">The functions included in this library help simplify a piece of code that looks like the following.</span></span>
  
```cs
XLOPER12 xMissing, xBool;
xMissing.xltype = xltypeMissing;
xBool.xltype = xltypeBool;
xBool.val.xbool = 0;
Excel12(xlcDisplay, 0, 2, (LPXLOPER12) &xMissing, (LPXLOPER12) &xBool);
```

<span data-ttu-id="8f68d-109">Le code simplifié ressemble à l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="8f68d-109">The simplified code looks like the following example.</span></span>
  
```cs
Excel12f(xlcDisplay, 0, 2, TempMissing12(), TempBool12(0));
```

<span data-ttu-id="8f68d-110">Les fonctions suivantes sont incluses dans la bibliothèque Framework :</span><span class="sxs-lookup"><span data-stu-id="8f68d-110">The following functions are included in the Framework library:</span></span>
  
||
|:-----|
|[<span data-ttu-id="8f68d-111">debugPrintf</span><span class="sxs-lookup"><span data-stu-id="8f68d-111">debugPrintf</span></span>](debugprintf.md) <br/> |
|<span data-ttu-id="8f68d-112">**GetTempMemory**</span><span class="sxs-lookup"><span data-stu-id="8f68d-112">**GetTempMemory**</span></span> <br/> |
|<span data-ttu-id="8f68d-113">**FreeAllTempMemory**</span><span class="sxs-lookup"><span data-stu-id="8f68d-113">**FreeAllTempMemory**</span></span> <br/> |
|[<span data-ttu-id="8f68d-114">InitFramework</span><span class="sxs-lookup"><span data-stu-id="8f68d-114">InitFramework</span></span>](initframework.md) <br/> |
|[<span data-ttu-id="8f68d-115">QuitFramework</span><span class="sxs-lookup"><span data-stu-id="8f68d-115">QuitFramework</span></span>](quitframework.md) <br/> |
   
|<span data-ttu-id="8f68d-116">**Fonctions utilisées avec XLOPER**</span><span class="sxs-lookup"><span data-stu-id="8f68d-116">**Functions Used with XLOPERs**</span></span>|<span data-ttu-id="8f68d-117">**Fonctions utilisées avec XLOPER12s**</span><span class="sxs-lookup"><span data-stu-id="8f68d-117">**Functions Used with XLOPER12s**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8f68d-118">Excel</span><span class="sxs-lookup"><span data-stu-id="8f68d-118">Excel</span></span>](excel-excel12f.md) <br/> |[<span data-ttu-id="8f68d-119">Excel12f</span><span class="sxs-lookup"><span data-stu-id="8f68d-119">Excel12f</span></span>](excel-excel12f.md) <br/> |
|[<span data-ttu-id="8f68d-120">TempNum</span><span class="sxs-lookup"><span data-stu-id="8f68d-120">TempNum</span></span>](tempnum-tempnum12.md) <br/> |[<span data-ttu-id="8f68d-121">TempNum12</span><span class="sxs-lookup"><span data-stu-id="8f68d-121">TempNum12</span></span>](tempnum-tempnum12.md) <br/> |
|[<span data-ttu-id="8f68d-122">TempStr</span><span class="sxs-lookup"><span data-stu-id="8f68d-122">TempStr</span></span>](tempstr.md) <br/> |[<span data-ttu-id="8f68d-123">TempStr12</span><span class="sxs-lookup"><span data-stu-id="8f68d-123">TempStr12</span></span>](tempstrconst-tempstr12.md) <br/> |
|[<span data-ttu-id="8f68d-124">TempStrConst</span><span class="sxs-lookup"><span data-stu-id="8f68d-124">TempStrConst</span></span>](tempstrconst-tempstr12.md) <br/> |[<span data-ttu-id="8f68d-125">TempStr12Const</span><span class="sxs-lookup"><span data-stu-id="8f68d-125">TempStr12Const</span></span>](tempstrconst-tempstr12.md) <br/> |
|[<span data-ttu-id="8f68d-126">TempBool</span><span class="sxs-lookup"><span data-stu-id="8f68d-126">TempBool</span></span>](tempbool-tempbool12.md) <br/> |[<span data-ttu-id="8f68d-127">TempBool12</span><span class="sxs-lookup"><span data-stu-id="8f68d-127">TempBool12</span></span>](tempbool-tempbool12.md) <br/> |
|[<span data-ttu-id="8f68d-128">TempInt</span><span class="sxs-lookup"><span data-stu-id="8f68d-128">TempInt</span></span>](tempint-tempint12.md) <br/> |[<span data-ttu-id="8f68d-129">TempInt12</span><span class="sxs-lookup"><span data-stu-id="8f68d-129">TempInt12</span></span>](tempint-tempint12.md) <br/> |
|[<span data-ttu-id="8f68d-130">TempErr</span><span class="sxs-lookup"><span data-stu-id="8f68d-130">TempErr</span></span>](temperr-temperr12.md) <br/> |[<span data-ttu-id="8f68d-131">TempErr12</span><span class="sxs-lookup"><span data-stu-id="8f68d-131">TempErr12</span></span>](temperr-temperr12.md) <br/> |
|[<span data-ttu-id="8f68d-132">TempActiveRef</span><span class="sxs-lookup"><span data-stu-id="8f68d-132">TempActiveRef</span></span>](tempactiveref-tempactiveref12.md) <br/> |[<span data-ttu-id="8f68d-133">TempActiveRef12</span><span class="sxs-lookup"><span data-stu-id="8f68d-133">TempActiveRef12</span></span>](tempactiveref-tempactiveref12.md) <br/> |
|[<span data-ttu-id="8f68d-134">TempActiveCell</span><span class="sxs-lookup"><span data-stu-id="8f68d-134">TempActiveCell</span></span>](tempactivecell-tempactivecell12.md) <br/> |[<span data-ttu-id="8f68d-135">TempActiveCell12</span><span class="sxs-lookup"><span data-stu-id="8f68d-135">TempActiveCell12</span></span>](tempactivecell-tempactivecell12.md) <br/> |
|[<span data-ttu-id="8f68d-136">TempActiveRow</span><span class="sxs-lookup"><span data-stu-id="8f68d-136">TempActiveRow</span></span>](tempactiverow-tempactiverow12.md) <br/> |[<span data-ttu-id="8f68d-137">TempActiveRow12</span><span class="sxs-lookup"><span data-stu-id="8f68d-137">TempActiveRow12</span></span>](tempactiverow-tempactiverow12.md) <br/> |
|[<span data-ttu-id="8f68d-138">TempActiveColumn</span><span class="sxs-lookup"><span data-stu-id="8f68d-138">TempActiveColumn</span></span>](tempactivecolumn-tempactivecolumn12.md) <br/> |[<span data-ttu-id="8f68d-139">TempActiveColumn12</span><span class="sxs-lookup"><span data-stu-id="8f68d-139">TempActiveColumn12</span></span>](tempactivecolumn-tempactivecolumn12.md) <br/> |
|[<span data-ttu-id="8f68d-140">TempMissing</span><span class="sxs-lookup"><span data-stu-id="8f68d-140">TempMissing</span></span>](tempmissing-tempmissing12.md) <br/> |[<span data-ttu-id="8f68d-141">TempMissing12</span><span class="sxs-lookup"><span data-stu-id="8f68d-141">TempMissing12</span></span>](tempmissing-tempmissing12.md) <br/> |
   
<span data-ttu-id="8f68d-142">Utilisation de ces fonctions réduit la quantité de temps nécessaire pour écrire une DLL ou XLL.</span><span class="sxs-lookup"><span data-stu-id="8f68d-142">Use of these functions shortens the amount of time required to write a DLL or XLL.</span></span> <span data-ttu-id="8f68d-143">Démarrer le développement de l’application exemple générique réduit également le temps de développement.</span><span class="sxs-lookup"><span data-stu-id="8f68d-143">Starting development from the sample application GENERIC also shortens development time.</span></span> <span data-ttu-id="8f68d-144">Utilisez générique. C en tant que modèle pour aider à configurer le cadre d’une solution XLL et remplacez le code existant avec vos propres.</span><span class="sxs-lookup"><span data-stu-id="8f68d-144">Use GENERIC.C as a template to help set up the framework of an XLL, and then replace the existing code with your own.</span></span>
  
<span data-ttu-id="8f68d-145">Le temporaire **XLOPER**/ fonctions**XLOPER12** créent **XLOPER**/ **XLOPER12** valeurs à l’aide de la mémoire à partir d’un segment de mémoire local géré par la bibliothèque de Framework.</span><span class="sxs-lookup"><span data-stu-id="8f68d-145">The temporary **XLOPER**/ **XLOPER12** functions create **XLOPER**/ **XLOPER12** values by using memory from a local heap managed by the Framework library.</span></span> <span data-ttu-id="8f68d-146">Le **XLOPER**/ **XLOPER12** valeurs restent valides jusqu'à ce que vous appelez la fonction **FreeAllTempMemory** ou une des fonctions **Excel** ou **Excel12f** .</span><span class="sxs-lookup"><span data-stu-id="8f68d-146">The **XLOPER**/ **XLOPER12** values remain valid until you call the **FreeAllTempMemory** function or either of the **Excel** or **Excel12f** functions.</span></span> <span data-ttu-id="8f68d-147">(Les fonctions **Excel** et **Excel12f** gratuit toute la mémoire temporaire avant de retourner).</span><span class="sxs-lookup"><span data-stu-id="8f68d-147">(The **Excel** and **Excel12f** functions free all temporary memory before returning.)</span></span> 
  
<span data-ttu-id="8f68d-148">Pour utiliser les fonctions de bibliothèque Framework, vous devez inclure le FRAMEWRK. H du fichier dans votre code C et ajoutez le FRAMEWRK. C ou FRMWRK32. Fichiers LIB à votre projet de code.</span><span class="sxs-lookup"><span data-stu-id="8f68d-148">To use the Framework library functions, you must include the FRAMEWRK.H file in your C code and add the FRAMEWRK.C or FRMWRK32.LIB files to your code project.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8f68d-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f68d-149">See also</span></span>

- [<span data-ttu-id="8f68d-150">R�f�rence des fonctions XLL SDK API Excel 2013</span><span class="sxs-lookup"><span data-stu-id="8f68d-150">Excel XLL SDK API Function Reference</span></span>](excel-xll-sdk-api-function-reference.md)

