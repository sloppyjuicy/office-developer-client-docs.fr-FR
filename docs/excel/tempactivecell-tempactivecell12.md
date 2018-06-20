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
- fonction tempactivecell12 [excel 2007], fonction TempActiveCell [Excel 2007]
localization_priority: Normal
ms.assetid: ac5a200d-32d5-4313-9a6d-d730032aaf10
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 8ad409a76195d67fa61e7991ce6527c40e0a3265
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782187"
---
# <a name="tempactivecelltempactivecell12"></a><span data-ttu-id="7724d-104">TempActiveCell/TempActiveCell12</span><span class="sxs-lookup"><span data-stu-id="7724d-104">TempActiveCell/TempActiveCell12</span></span>

 <span data-ttu-id="7724d-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7724d-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="7724d-106">Fonctions de la bibliothèque Framework qui créent un temporaire **XLOPER**/ **XLOPER12** contenant une référence à une cellule dans la feuille active.</span><span class="sxs-lookup"><span data-stu-id="7724d-106">Framework library functions that create a temporary **XLOPER**/ **XLOPER12** containing an external reference to a cell on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveCell(WORD row, BYTE col);
LPXLOPER12 TempActiveCell12(RW row, COL co);
```

## <a name="parameters"></a><span data-ttu-id="7724d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7724d-107">Parameters</span></span>

 <span data-ttu-id="7724d-108">_ligne_</span><span class="sxs-lookup"><span data-stu-id="7724d-108">_row_</span></span>
  
<span data-ttu-id="7724d-109">La ligne à référencer.</span><span class="sxs-lookup"><span data-stu-id="7724d-109">The row to be referenced.</span></span> <span data-ttu-id="7724d-110">Arguments de ligne commencent par zéro afin que la ligne 1 est transmise en tant que 0.</span><span class="sxs-lookup"><span data-stu-id="7724d-110">Row arguments are zero-based so that row 1 is passed as 0.</span></span> <span data-ttu-id="7724d-111">Dans Microsoft Office Excel 2003 et les précédentes versions et à compter d’Excel 2007 en cours d’exécution un classeur en mode de compatibilité, la valeur maximale est 65 535 = 2 ^ 16-1 et la valeur maximale qui peut être effectuée par un nombre entier de WORD.</span><span class="sxs-lookup"><span data-stu-id="7724d-111">In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 65,535 = 2^16 - 1 and is the maximum value that can be taken by a WORD integer.</span></span> <span data-ttu-id="7724d-112">À compter d’Excel 2007, un classeur en cours d’exécution, la valeur maximale est de 1 048 575 = 2 ^ 20-1.</span><span class="sxs-lookup"><span data-stu-id="7724d-112">Starting in Excel 2007 running a workbook, the maximum value is 1,048,575 = 2^20 - 1.</span></span> <span data-ttu-id="7724d-113">RW est défini comme un entier signé 32 bits dans XLCALL. H.</span><span class="sxs-lookup"><span data-stu-id="7724d-113">RW is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
 <span data-ttu-id="7724d-114">_col_</span><span class="sxs-lookup"><span data-stu-id="7724d-114">_col_</span></span>
  
<span data-ttu-id="7724d-115">La colonne à référencer.</span><span class="sxs-lookup"><span data-stu-id="7724d-115">The column to be referenced.</span></span> <span data-ttu-id="7724d-116">Il s’agit en partant de zéro afin que la colonne A est transmise en tant que 0.</span><span class="sxs-lookup"><span data-stu-id="7724d-116">This is zero-based so that column A is passed as 0.</span></span> <span data-ttu-id="7724d-117">Dans Excel 2003 et les précédentes versions et à compter d’Excel 2007 en cours d’exécution un classeur en mode de compatibilité, la valeur maximale est de 255 = 2 ^ 8-1 et la valeur maximale qui peut être effectuée par un entier.</span><span class="sxs-lookup"><span data-stu-id="7724d-117">In Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 255 = 2^8 - 1 and is the maximum value that can be taken by a BYTE integer.</span></span> <span data-ttu-id="7724d-118">À compter d’Excel 2007, un classeur en cours d’exécution, la valeur maximale est de 16 383 = 2 ^ 14-1.</span><span class="sxs-lookup"><span data-stu-id="7724d-118">Starting in Excel 2007 running a workbook, the maximum value is 16,383 = 2^14 - 1.</span></span> <span data-ttu-id="7724d-119">COL est défini comme un entier signé 32 bits dans XLCALL. H.</span><span class="sxs-lookup"><span data-stu-id="7724d-119">COL is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="7724d-120">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="7724d-120">Return value</span></span>

<span data-ttu-id="7724d-121">Renvoie une référence externe **xltypeRef** à la cellule passée.</span><span class="sxs-lookup"><span data-stu-id="7724d-121">Returns an **xltypeRef** external reference to the cell passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="7724d-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="7724d-122">Example</span></span>

<span data-ttu-id="7724d-123">L’exemple suivant utilise **TempActiveCell12** pour afficher le contenu de B94 dans la feuille active.</span><span class="sxs-lookup"><span data-stu-id="7724d-123">The following example uses **TempActiveCell12** to display the contents of B94 on the active sheet.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveCellExample(void)
{
   Excel12f(xlcAlert, 0, 1, TempActiveCell12(93,1));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="7724d-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7724d-124">See also</span></span>



[<span data-ttu-id="7724d-125">Fonctions de la bibliothèque Framework</span><span class="sxs-lookup"><span data-stu-id="7724d-125">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

