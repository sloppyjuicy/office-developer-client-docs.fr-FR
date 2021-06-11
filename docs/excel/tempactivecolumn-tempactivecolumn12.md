---
title: TempActiveColumn/TempActiveColumn12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveColumn
- TempActiveColumn12
keywords:
- fonction tempactivecolumn12 [excel 2007],TempActiveColumn function [Excel 2007]
localization_priority: Normal
ms.assetid: 4b1f34c4-e7fa-4a0b-8fc5-c9d465ebb70c
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d1399a407e3e269b78c7afbde8ff32c126b4b1bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417874"
---
# <a name="tempactivecolumntempactivecolumn12"></a><span data-ttu-id="033b3-104">TempActiveColumn/TempActiveColumn12</span><span class="sxs-lookup"><span data-stu-id="033b3-104">TempActiveColumn/TempActiveColumn12</span></span>

 <span data-ttu-id="033b3-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="033b3-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="033b3-106">Fonctions de bibliothèque d’infrastructure qui créent une **XLOPER** /  **XLOPER12** temporaire contenant une référence externe à une colonne entière de la feuille active.</span><span class="sxs-lookup"><span data-stu-id="033b3-106">Framework library functions that create a temporary **XLOPER**/ **XLOPER12** containing an external reference to an entire column on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveColumn(BYTE col);
LPXLOPER12 TempActiveColumn12(COL col);
```

## <a name="parameters"></a><span data-ttu-id="033b3-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="033b3-107">Parameters</span></span>

 <span data-ttu-id="033b3-108">_col_ (**BYTE**)</span><span class="sxs-lookup"><span data-stu-id="033b3-108">_col_ (**BYTE**)</span></span>
  
<span data-ttu-id="033b3-109">Colonne à référencer.</span><span class="sxs-lookup"><span data-stu-id="033b3-109">The column to be referenced.</span></span> <span data-ttu-id="033b3-110">Il s’agit d’une valeur de base zéro afin que la colonne A soit passée sous la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="033b3-110">This is zero-based so that column A is passed as 0.</span></span> <span data-ttu-id="033b3-111">Dans Microsoft Office Excel 2003 et versions antérieures, et à partir de Excel 2007 exécutant un livre de travail en mode de compatibilité, la valeur maximale est 255 = 2^8 - 1 et est la valeur maximale qui peut être prise par un nombre d’nombres byTE.</span><span class="sxs-lookup"><span data-stu-id="033b3-111">In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 255 = 2^8 - 1 and is the maximum value that can be taken by a BYTE integer.</span></span> <span data-ttu-id="033b3-112">À partir Excel 2007 exécutant un manuel, la valeur maximale est 16 383 = 2^14 - 1.</span><span class="sxs-lookup"><span data-stu-id="033b3-112">Starting in Excel 2007 running a workbook, the maximum value is 16,383 = 2^14 - 1.</span></span> <span data-ttu-id="033b3-113">Col est défini comme un integer signé 32 bits dans XLCALL.H.</span><span class="sxs-lookup"><span data-stu-id="033b3-113">COL is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="033b3-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="033b3-114">Return value</span></span>

<span data-ttu-id="033b3-115">Renvoie une **référence externe xltypeRef** à la colonne transmise.</span><span class="sxs-lookup"><span data-stu-id="033b3-115">Returns an **xltypeRef** external reference to the column passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="033b3-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="033b3-116">Example</span></span>

<span data-ttu-id="033b3-117">L’exemple suivant **utilise TempActiveColumn12** pour sélectionner la colonne entière B.</span><span class="sxs-lookup"><span data-stu-id="033b3-117">The following example uses **TempActiveColumn12** to select the entire column B.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveColumnExample(void)
{
    Excel12f(xlcSelect, 0, 1, TempActiveColumn12(1));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="033b3-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="033b3-118">See also</span></span>



[<span data-ttu-id="033b3-119">Fonctions de la bibliothèque Framework</span><span class="sxs-lookup"><span data-stu-id="033b3-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

