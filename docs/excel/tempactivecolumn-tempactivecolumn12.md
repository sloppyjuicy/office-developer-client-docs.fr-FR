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
- fonction tempactivecolumn12 [excel 2007], fonction TempActiveColumn [Excel 2007]
localization_priority: Normal
ms.assetid: 4b1f34c4-e7fa-4a0b-8fc5-c9d465ebb70c
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: ac3dbb0bb43527f790e6934d73bee30a33f8555f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782193"
---
# <a name="tempactivecolumntempactivecolumn12"></a><span data-ttu-id="75b92-104">TempActiveColumn/TempActiveColumn12</span><span class="sxs-lookup"><span data-stu-id="75b92-104">TempActiveColumn/TempActiveColumn12</span></span>

 <span data-ttu-id="75b92-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="75b92-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="75b92-106">Fonctions de la bibliothèque Framework qui créent un temporaire **XLOPER**/ **XLOPER12** contenant une référence à une colonne entière de la feuille active.</span><span class="sxs-lookup"><span data-stu-id="75b92-106">Framework library functions that create a temporary **XLOPER**/ **XLOPER12** containing an external reference to an entire column on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveColumn(BYTE col);
LPXLOPER12 TempActiveColumn12(COL col);
```

## <a name="parameters"></a><span data-ttu-id="75b92-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="75b92-107">Parameters</span></span>

 <span data-ttu-id="75b92-108">_col_ (**Octets**)</span><span class="sxs-lookup"><span data-stu-id="75b92-108">_col_ (**BYTE**)</span></span>
  
<span data-ttu-id="75b92-109">La colonne à référencer.</span><span class="sxs-lookup"><span data-stu-id="75b92-109">The column to be referenced.</span></span> <span data-ttu-id="75b92-110">Il s’agit en partant de zéro afin que la colonne A est transmise en tant que 0.</span><span class="sxs-lookup"><span data-stu-id="75b92-110">This is zero-based so that column A is passed as 0.</span></span> <span data-ttu-id="75b92-111">Dans Microsoft Office Excel 2003 et les précédentes versions et à compter d’Excel 2007 en cours d’exécution un classeur en mode de compatibilité, la valeur maximale est de 255 = 2 ^ 8-1 et la valeur maximale qui peut être effectuée par un entier.</span><span class="sxs-lookup"><span data-stu-id="75b92-111">In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 255 = 2^8 - 1 and is the maximum value that can be taken by a BYTE integer.</span></span> <span data-ttu-id="75b92-112">À compter d’Excel 2007, un classeur en cours d’exécution, la valeur maximale est de 16 383 = 2 ^ 14-1.</span><span class="sxs-lookup"><span data-stu-id="75b92-112">Starting in Excel 2007 running a workbook, the maximum value is 16,383 = 2^14 - 1.</span></span> <span data-ttu-id="75b92-113">COL est défini comme un entier signé 32 bits dans XLCALL. H.</span><span class="sxs-lookup"><span data-stu-id="75b92-113">COL is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="75b92-114">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="75b92-114">Return value</span></span>

<span data-ttu-id="75b92-115">Renvoie une référence externe **xltypeRef** à la colonne passée.</span><span class="sxs-lookup"><span data-stu-id="75b92-115">Returns an **xltypeRef** external reference to the column passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="75b92-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="75b92-116">Example</span></span>

<span data-ttu-id="75b92-117">L’exemple suivant utilise **TempActiveColumn12** pour sélectionner toute la colonne B.</span><span class="sxs-lookup"><span data-stu-id="75b92-117">The following example uses **TempActiveColumn12** to select the entire column B.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveColumnExample(void)
{
    Excel12f(xlcSelect, 0, 1, TempActiveColumn12(1));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="75b92-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75b92-118">See also</span></span>



[<span data-ttu-id="75b92-119">Fonctions de la bibliothèque Framework</span><span class="sxs-lookup"><span data-stu-id="75b92-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

