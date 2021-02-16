---
title: TempActiveCell/TempActiveCell12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveCell
- TempActiveCell12
keywords:
- fonction tempactivecell12 [excel 2007],fonction TempActiveCell [Excel 2007]
localization_priority: Normal
ms.assetid: ac5a200d-32d5-4313-9a6d-d730032aaf10
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f9bdb4cd9919d0e52654a3996ede99c4d1b35cc6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413191"
---
# <a name="tempactivecelltempactivecell12"></a><span data-ttu-id="a5a01-104">TempActiveCell/TempActiveCell12</span><span class="sxs-lookup"><span data-stu-id="a5a01-104">TempActiveCell/TempActiveCell12</span></span>

 <span data-ttu-id="a5a01-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a5a01-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a5a01-106">Fonctions de bibliothèque d’infrastructure qui créent une **XLOPER XLOPER12** temporaire contenant une référence externe à une cellule /   de la feuille active.</span><span class="sxs-lookup"><span data-stu-id="a5a01-106">Framework library functions that create a temporary **XLOPER**/ **XLOPER12** containing an external reference to a cell on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveCell(WORD row, BYTE col);
LPXLOPER12 TempActiveCell12(RW row, COL co);
```

## <a name="parameters"></a><span data-ttu-id="a5a01-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a5a01-107">Parameters</span></span>

 <span data-ttu-id="a5a01-108">_row_</span><span class="sxs-lookup"><span data-stu-id="a5a01-108">_row_</span></span>
  
<span data-ttu-id="a5a01-109">Ligne à référencer.</span><span class="sxs-lookup"><span data-stu-id="a5a01-109">The row to be referenced.</span></span> <span data-ttu-id="a5a01-110">Les arguments de ligne sont basés sur zéro afin que la ligne 1 soit passée en tant que 0.</span><span class="sxs-lookup"><span data-stu-id="a5a01-110">Row arguments are zero-based so that row 1 is passed as 0.</span></span> <span data-ttu-id="a5a01-111">Dans Microsoft Office Excel 2003 et versions antérieures, et à partir d’Excel 2007 exécutant un livre de calcul en mode de compatibilité, la valeur maximale est 65 535 = 2^16 - 1 et est la valeur maximale qui peut être prise par un nombre total WORD.</span><span class="sxs-lookup"><span data-stu-id="a5a01-111">In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 65,535 = 2^16 - 1 and is the maximum value that can be taken by a WORD integer.</span></span> <span data-ttu-id="a5a01-112">À partir d’Excel 2007 exécutant un workbook, la valeur maximale est 1 048 575 = 2^20 - 1.</span><span class="sxs-lookup"><span data-stu-id="a5a01-112">Starting in Excel 2007 running a workbook, the maximum value is 1,048,575 = 2^20 - 1.</span></span> <span data-ttu-id="a5a01-113">RW est défini comme un integer signé 32 bits dans XLCALL.H.</span><span class="sxs-lookup"><span data-stu-id="a5a01-113">RW is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
 <span data-ttu-id="a5a01-114">_col_</span><span class="sxs-lookup"><span data-stu-id="a5a01-114">_col_</span></span>
  
<span data-ttu-id="a5a01-115">Colonne à référencer.</span><span class="sxs-lookup"><span data-stu-id="a5a01-115">The column to be referenced.</span></span> <span data-ttu-id="a5a01-116">En fonction de zéro, la colonne A est passée sous la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="a5a01-116">This is zero-based so that column A is passed as 0.</span></span> <span data-ttu-id="a5a01-117">Dans Excel 2003 et versions antérieures, et à partir d’Excel 2007 exécutant un workbook en mode de compatibilité, la valeur maximale est 255 = 2^8 - 1 et est la valeur maximale qui peut être prise par un nombre d’nombres byTE.</span><span class="sxs-lookup"><span data-stu-id="a5a01-117">In Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 255 = 2^8 - 1 and is the maximum value that can be taken by a BYTE integer.</span></span> <span data-ttu-id="a5a01-118">À partir d’Excel 2007 exécutant un workbook, la valeur maximale est 16 383 = 2^14 - 1.</span><span class="sxs-lookup"><span data-stu-id="a5a01-118">Starting in Excel 2007 running a workbook, the maximum value is 16,383 = 2^14 - 1.</span></span> <span data-ttu-id="a5a01-119">Col est défini comme un integer signé 32 bits dans XLCALL.H.</span><span class="sxs-lookup"><span data-stu-id="a5a01-119">COL is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="a5a01-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a5a01-120">Return value</span></span>

<span data-ttu-id="a5a01-121">Renvoie une **référence externe xltypeRef** à la cellule transmise.</span><span class="sxs-lookup"><span data-stu-id="a5a01-121">Returns an **xltypeRef** external reference to the cell passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="a5a01-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="a5a01-122">Example</span></span>

<span data-ttu-id="a5a01-123">L’exemple suivant **utilise TempActiveCell12** pour afficher le contenu de B94 sur la feuille active.</span><span class="sxs-lookup"><span data-stu-id="a5a01-123">The following example uses **TempActiveCell12** to display the contents of B94 on the active sheet.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveCellExample(void)
{
   Excel12f(xlcAlert, 0, 1, TempActiveCell12(93,1));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="a5a01-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5a01-124">See also</span></span>



[<span data-ttu-id="a5a01-125">Fonctions de la bibliothèque Framework</span><span class="sxs-lookup"><span data-stu-id="a5a01-125">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

