---
title: TempActiveRef/TempActiveRef12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveRef
- TempActiveRef12
keywords:
- fonction tempactiveref [excel 2007],TempActiveRef12 function [Excel 2007]
localization_priority: Normal
ms.assetid: 7c69d15a-294b-4545-983b-720409001e0e
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 58feee8f43e0f90f710c9e4387684dcb6d173a7b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415543"
---
# <a name="tempactivereftempactiveref12"></a><span data-ttu-id="b8149-104">TempActiveRef/TempActiveRef12</span><span class="sxs-lookup"><span data-stu-id="b8149-104">TempActiveRef/TempActiveRef12</span></span>

 <span data-ttu-id="b8149-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b8149-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="b8149-106">Fonction de bibliothèque d’infrastructure qui crée une **xlOPER** /  **XLOPER12** temporaire contenant une référence externe à un bloc rectangulaire de cellules sur la feuille active.</span><span class="sxs-lookup"><span data-stu-id="b8149-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing an external reference to rectangular block of cells on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveRef(WORD rwFirst, WORD rwLast, BYTE colFirst, BYTE colLast);
LPXLOPER12 TempActiveRef12(ROW rwFirst, ROW rwLast, COL colFirst, COL colLast);
```

## <a name="parameters"></a><span data-ttu-id="b8149-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="b8149-107">Parameters</span></span>

 <span data-ttu-id="b8149-108">_rwFirst_</span><span class="sxs-lookup"><span data-stu-id="b8149-108">_rwFirst_</span></span>
  
<span data-ttu-id="b8149-109">Ligne de début de la référence.</span><span class="sxs-lookup"><span data-stu-id="b8149-109">The starting row of the reference.</span></span>
  
 <span data-ttu-id="b8149-110">_rwLast_</span><span class="sxs-lookup"><span data-stu-id="b8149-110">_rwLast_</span></span>
  
<span data-ttu-id="b8149-111">Ligne de fin de la référence.</span><span class="sxs-lookup"><span data-stu-id="b8149-111">The ending row of the reference.</span></span>
  
<span data-ttu-id="b8149-112">Les arguments de ligne sont basés sur zéro afin que la ligne 1 soit passée en tant que 0.</span><span class="sxs-lookup"><span data-stu-id="b8149-112">Row arguments are zero-based so that row 1 is passed as 0.</span></span> <span data-ttu-id="b8149-113">Dans Microsoft Office Excel 2003 et versions antérieures, et à partir de Excel 2007 exécutant un livre de travail en mode de compatibilité, la valeur maximale est 65 535 = 2^16 - 1 et est la valeur maximale qui peut être prise par un nombre total WORD.</span><span class="sxs-lookup"><span data-stu-id="b8149-113">In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 65,535 = 2^16 - 1 and is the maximum value that can be taken by a WORD integer.</span></span> <span data-ttu-id="b8149-114">À compter Excel 2007 exécutant un manuel, la valeur maximale est 1 048 575 = 2^20 - 1.</span><span class="sxs-lookup"><span data-stu-id="b8149-114">Starting in Excel 2007 running a workbook, the maximum value is 1,048,575 = 2^20 - 1.</span></span> <span data-ttu-id="b8149-115">RW est défini comme un integer signé 32 bits dans XLCALL.H.</span><span class="sxs-lookup"><span data-stu-id="b8149-115">RW is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
 <span data-ttu-id="b8149-116">_colFirst_</span><span class="sxs-lookup"><span data-stu-id="b8149-116">_colFirst_</span></span>
  
<span data-ttu-id="b8149-117">Numéro de colonne de début de la référence.</span><span class="sxs-lookup"><span data-stu-id="b8149-117">The starting column number of the reference.</span></span>
  
 <span data-ttu-id="b8149-118">_colLast_</span><span class="sxs-lookup"><span data-stu-id="b8149-118">_colLast_</span></span>
  
<span data-ttu-id="b8149-119">Numéro de colonne de fin de la référence.</span><span class="sxs-lookup"><span data-stu-id="b8149-119">The ending column number of the reference.</span></span>
  
<span data-ttu-id="b8149-120">Les arguments de colonne sont basés sur zéro afin que la colonne A soit passée sous la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="b8149-120">Column arguments are zero-based so that column A is passed as 0.</span></span> <span data-ttu-id="b8149-121">Dans Excel 2003 et versions antérieures, et à partir de Excel 2007 exécutant un livre de travail en mode de compatibilité, la valeur maximale est 255 = 2^8 - 1 et est la valeur maximale qui peut être prise par un nombre d’nombres byTE.</span><span class="sxs-lookup"><span data-stu-id="b8149-121">In Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 255 = 2^8 - 1 and is the maximum value that can be taken by a BYTE integer.</span></span> <span data-ttu-id="b8149-122">À partir Excel 2007 exécutant un manuel, la valeur maximale est 16 383 = 2^14 - 1.</span><span class="sxs-lookup"><span data-stu-id="b8149-122">Starting in Excel 2007 running a workbook, the maximum value is 16,383 = 2^14 - 1.</span></span> <span data-ttu-id="b8149-123">Col est défini comme un integer signé 32 bits dans XLCALL.H.</span><span class="sxs-lookup"><span data-stu-id="b8149-123">COL is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="b8149-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b8149-124">Return value</span></span>

<span data-ttu-id="b8149-125">Renvoie une **référence externe xltypeRef** à un bloc rectangulaire de cellules transmises.</span><span class="sxs-lookup"><span data-stu-id="b8149-125">Returns an **xltypeRef** external reference to rectangular block of cells passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="b8149-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="b8149-126">Example</span></span>

<span data-ttu-id="b8149-127">Cet exemple utilise la **fonction TempActiveRef12** pour sélectionner les cellules A105:C110.</span><span class="sxs-lookup"><span data-stu-id="b8149-127">This example uses the **TempActiveRef12** function to select cells A105:C110.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveRefExample(void)
{
    Excel12f(xlcSelect, 0, 1, TempActiveRef12(104, 109, 0, 2));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="b8149-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8149-128">See also</span></span>



[<span data-ttu-id="b8149-129">Fonctions de la bibliothèque Framework</span><span class="sxs-lookup"><span data-stu-id="b8149-129">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

