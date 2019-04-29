---
title: TempActiveRow/TempActiveRow12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveRow
- TempActiveRow12
keywords:
- fonction tempactiverow [Excel 2007], fonction TempActiveRow12 [Excel 2007]
localization_priority: Normal
ms.assetid: cbb9181c-59b0-4133-a085-94a94ac3f229
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 1f89c458a521b41e4f172f8a6c53526440bb472b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413107"
---
# <a name="tempactiverowtempactiverow12"></a><span data-ttu-id="fd5c5-104">TempActiveRow/TempActiveRow12</span><span class="sxs-lookup"><span data-stu-id="fd5c5-104">TempActiveRow/TempActiveRow12</span></span>

 <span data-ttu-id="fd5c5-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="fd5c5-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="fd5c5-106">Fonctions de la bibliothèque d'infrastructure qui créent une liste **XLOPER**/ \*\*\*\* temporaire contenant une référence externe à une ligne entière dans la feuille active.</span><span class="sxs-lookup"><span data-stu-id="fd5c5-106">Framework library functions that create a temporary **XLOPER**/ **XLOPER12** containing an external reference to an entire row on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveRow(WORD row);
LPXLOPER12 TempActiveRow12(ROW row);
```

## <a name="parameters"></a><span data-ttu-id="fd5c5-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fd5c5-107">Parameters</span></span>

 <span data-ttu-id="fd5c5-108">_colonne_</span><span class="sxs-lookup"><span data-stu-id="fd5c5-108">_row_</span></span>
  
<span data-ttu-id="fd5c5-109">Ligne à référencer.</span><span class="sxs-lookup"><span data-stu-id="fd5c5-109">The row to be referenced.</span></span> <span data-ttu-id="fd5c5-110">Les arguments de ligne sont basés sur zéro de sorte que la ligne 1 est transmise à 0.</span><span class="sxs-lookup"><span data-stu-id="fd5c5-110">Row arguments are zero-based so that row 1 is passed as 0.</span></span> <span data-ttu-id="fd5c5-111">Dans Microsoft Office Excel 2003 et les versions antérieures, et en commençant dans Excel 2007 exécutant un classeur en mode de compatibilité, la valeur maximale est 65 535 = 2 ^ 16-1 et représente la valeur maximale pouvant être prise par un entier de mot.</span><span class="sxs-lookup"><span data-stu-id="fd5c5-111">In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 65,535 = 2^16 - 1 and is the maximum value that can be taken by a WORD integer.</span></span> <span data-ttu-id="fd5c5-112">À partir d'Excel 2007 exécutant un classeur, la valeur maximale est 1 048 575 = 2 ^ 20-1.</span><span class="sxs-lookup"><span data-stu-id="fd5c5-112">Starting in Excel 2007 running a workbook, the maximum value is 1,048,575 = 2^20 - 1.</span></span> <span data-ttu-id="fd5c5-113">RW est défini comme un entier signé 32 bits dans XLCALL. H.</span><span class="sxs-lookup"><span data-stu-id="fd5c5-113">RW is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="fd5c5-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fd5c5-114">Return value</span></span>

<span data-ttu-id="fd5c5-115">Renvoie une référence externe **xltypeRef** aux cellules de ligne transmises.</span><span class="sxs-lookup"><span data-stu-id="fd5c5-115">Returns an **xltypeRef** external reference to row cells passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="fd5c5-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="fd5c5-116">Example</span></span>

<span data-ttu-id="fd5c5-117">Cet exemple utilise la fonction **TempActiveRow12** pour sélectionner la ligne 113.</span><span class="sxs-lookup"><span data-stu-id="fd5c5-117">This example uses the **TempActiveRow12** function to select row 113.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveRowExample(void)
{
   Excel12f(xlcSelect, 0, 1, TempActiveRow12(112));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="fd5c5-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd5c5-118">See also</span></span>



[<span data-ttu-id="fd5c5-119">Fonctions de la bibliothèque Framework</span><span class="sxs-lookup"><span data-stu-id="fd5c5-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

