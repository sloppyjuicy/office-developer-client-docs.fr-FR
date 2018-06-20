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
- fonction tempactiverow [excel 2007], fonction TempActiveRow12 [Excel 2007]
localization_priority: Normal
ms.assetid: cbb9181c-59b0-4133-a085-94a94ac3f229
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: a406d6e5a8ffa91e103276cb39230058b4840614
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782188"
---
# <a name="tempactiverowtempactiverow12"></a><span data-ttu-id="e634f-104">TempActiveRow/TempActiveRow12</span><span class="sxs-lookup"><span data-stu-id="e634f-104">TempActiveRow/TempActiveRow12</span></span>

 <span data-ttu-id="e634f-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e634f-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="e634f-106">Fonctions de la bibliothèque Framework qui créent un temporaire **XLOPER**/ **XLOPER12** contenant une référence à une ligne entière de la feuille active.</span><span class="sxs-lookup"><span data-stu-id="e634f-106">Framework library functions that create a temporary **XLOPER**/ **XLOPER12** containing an external reference to an entire row on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveRow(WORD row);
LPXLOPER12 TempActiveRow12(ROW row);
```

## <a name="parameters"></a><span data-ttu-id="e634f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e634f-107">Parameters</span></span>

 <span data-ttu-id="e634f-108">_ligne_</span><span class="sxs-lookup"><span data-stu-id="e634f-108">_row_</span></span>
  
<span data-ttu-id="e634f-109">La ligne à référencer.</span><span class="sxs-lookup"><span data-stu-id="e634f-109">The row to be referenced.</span></span> <span data-ttu-id="e634f-110">Arguments de ligne commencent par zéro afin que la ligne 1 est transmise en tant que 0.</span><span class="sxs-lookup"><span data-stu-id="e634f-110">Row arguments are zero-based so that row 1 is passed as 0.</span></span> <span data-ttu-id="e634f-111">Dans Microsoft Office Excel 2003 et les précédentes versions et à compter d’Excel 2007 en cours d’exécution un classeur en mode de compatibilité, la valeur maximale est 65 535 = 2 ^ 16-1 et la valeur maximale qui peut être effectuée par un nombre entier de WORD.</span><span class="sxs-lookup"><span data-stu-id="e634f-111">In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 65,535 = 2^16 - 1 and is the maximum value that can be taken by a WORD integer.</span></span> <span data-ttu-id="e634f-112">À compter d’Excel 2007, un classeur en cours d’exécution, la valeur maximale est de 1 048 575 = 2 ^ 20-1.</span><span class="sxs-lookup"><span data-stu-id="e634f-112">Starting in Excel 2007 running a workbook, the maximum value is 1,048,575 = 2^20 - 1.</span></span> <span data-ttu-id="e634f-113">RW est défini comme un entier signé 32 bits dans XLCALL. H.</span><span class="sxs-lookup"><span data-stu-id="e634f-113">RW is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="e634f-114">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="e634f-114">Return value</span></span>

<span data-ttu-id="e634f-115">Renvoie une référence externe **xltypeRef** aux cellules de ligne passé.</span><span class="sxs-lookup"><span data-stu-id="e634f-115">Returns an **xltypeRef** external reference to row cells passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="e634f-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="e634f-116">Example</span></span>

<span data-ttu-id="e634f-117">Cet exemple utilise la fonction **TempActiveRow12** pour sélectionner ligne 113.</span><span class="sxs-lookup"><span data-stu-id="e634f-117">This example uses the **TempActiveRow12** function to select row 113.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveRowExample(void)
{
   Excel12f(xlcSelect, 0, 1, TempActiveRow12(112));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="e634f-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e634f-118">See also</span></span>



[<span data-ttu-id="e634f-119">Fonctions de la bibliothèque Framework</span><span class="sxs-lookup"><span data-stu-id="e634f-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

