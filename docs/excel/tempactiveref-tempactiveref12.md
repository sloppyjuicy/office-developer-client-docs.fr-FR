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
- fonction tempactiveref [excel 2007], fonction TempActiveRef12 [Excel 2007]
localization_priority: Normal
ms.assetid: 7c69d15a-294b-4545-983b-720409001e0e
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 5c2e82dcaf9bf562048b5d2582ece1bd262b47eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782190"
---
# <a name="tempactivereftempactiveref12"></a><span data-ttu-id="4153a-104">TempActiveRef/TempActiveRef12</span><span class="sxs-lookup"><span data-stu-id="4153a-104">TempActiveRef/TempActiveRef12</span></span>

 <span data-ttu-id="4153a-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4153a-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="4153a-106">Fonction de bibliothèque Framework crée un temporaire **XLOPER**/ **XLOPER12** contenant une référence à un bloc rectangulaire de cellules dans la feuille active.</span><span class="sxs-lookup"><span data-stu-id="4153a-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing an external reference to rectangular block of cells on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveRef(WORD rwFirst, WORD rwLast, BYTE colFirst, BYTE colLast);
LPXLOPER12 TempActiveRef12(ROW rwFirst, ROW rwLast, COL colFirst, COL colLast);
```

## <a name="parameters"></a><span data-ttu-id="4153a-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4153a-107">Parameters</span></span>

 <span data-ttu-id="4153a-108">_rwFirst_</span><span class="sxs-lookup"><span data-stu-id="4153a-108">_rwFirst_</span></span>
  
<span data-ttu-id="4153a-109">La ligne de début de la référence.</span><span class="sxs-lookup"><span data-stu-id="4153a-109">The starting row of the reference.</span></span>
  
 <span data-ttu-id="4153a-110">_rwLast_</span><span class="sxs-lookup"><span data-stu-id="4153a-110">_rwLast_</span></span>
  
<span data-ttu-id="4153a-111">La ligne de fin de la référence.</span><span class="sxs-lookup"><span data-stu-id="4153a-111">The ending row of the reference.</span></span>
  
<span data-ttu-id="4153a-112">Arguments de ligne commencent par zéro afin que la ligne 1 est transmise en tant que 0.</span><span class="sxs-lookup"><span data-stu-id="4153a-112">Row arguments are zero-based so that row 1 is passed as 0.</span></span> <span data-ttu-id="4153a-113">Dans Microsoft Office Excel 2003 et les précédentes versions et à compter d’Excel 2007 en cours d’exécution un classeur en mode de compatibilité, la valeur maximale est 65 535 = 2 ^ 16-1 et la valeur maximale qui peut être effectuée par un nombre entier de WORD.</span><span class="sxs-lookup"><span data-stu-id="4153a-113">In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 65,535 = 2^16 - 1 and is the maximum value that can be taken by a WORD integer.</span></span> <span data-ttu-id="4153a-114">À compter d’Excel 2007, un classeur en cours d’exécution, la valeur maximale est de 1 048 575 = 2 ^ 20-1.</span><span class="sxs-lookup"><span data-stu-id="4153a-114">Starting in Excel 2007 running a workbook, the maximum value is 1,048,575 = 2^20 - 1.</span></span> <span data-ttu-id="4153a-115">RW est défini comme un entier signé 32 bits dans XLCALL. H.</span><span class="sxs-lookup"><span data-stu-id="4153a-115">RW is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
 <span data-ttu-id="4153a-116">_colFirst_</span><span class="sxs-lookup"><span data-stu-id="4153a-116">_colFirst_</span></span>
  
<span data-ttu-id="4153a-117">Le numéro de colonne de départ de la référence.</span><span class="sxs-lookup"><span data-stu-id="4153a-117">The starting column number of the reference.</span></span>
  
 <span data-ttu-id="4153a-118">_colLast_</span><span class="sxs-lookup"><span data-stu-id="4153a-118">_colLast_</span></span>
  
<span data-ttu-id="4153a-119">Numéro de colonne de fin de la référence.</span><span class="sxs-lookup"><span data-stu-id="4153a-119">The ending column number of the reference.</span></span>
  
<span data-ttu-id="4153a-120">Arguments de colonne sont de base zéro afin que la colonne A est transmise en tant que 0.</span><span class="sxs-lookup"><span data-stu-id="4153a-120">Column arguments are zero-based so that column A is passed as 0.</span></span> <span data-ttu-id="4153a-121">Dans Excel 2003 et les précédentes versions et à compter d’Excel 2007 en cours d’exécution un classeur en mode de compatibilité, la valeur maximale est de 255 = 2 ^ 8-1 et la valeur maximale qui peut être effectuée par un entier.</span><span class="sxs-lookup"><span data-stu-id="4153a-121">In Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 255 = 2^8 - 1 and is the maximum value that can be taken by a BYTE integer.</span></span> <span data-ttu-id="4153a-122">À compter d’Excel 2007, un classeur en cours d’exécution, la valeur maximale est de 16 383 = 2 ^ 14-1.</span><span class="sxs-lookup"><span data-stu-id="4153a-122">Starting in Excel 2007 running a workbook, the maximum value is 16,383 = 2^14 - 1.</span></span> <span data-ttu-id="4153a-123">COL est défini comme un entier signé 32 bits dans XLCALL. H.</span><span class="sxs-lookup"><span data-stu-id="4153a-123">COL is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="4153a-124">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="4153a-124">Return value</span></span>

<span data-ttu-id="4153a-125">Renvoie une référence externe **xltypeRef** au bloc de cellules passé rectangulaire.</span><span class="sxs-lookup"><span data-stu-id="4153a-125">Returns an **xltypeRef** external reference to rectangular block of cells passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="4153a-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="4153a-126">Example</span></span>

<span data-ttu-id="4153a-127">Cet exemple utilise la fonction **TempActiveRef12** pour sélectionner les cellules A105:C110.</span><span class="sxs-lookup"><span data-stu-id="4153a-127">This example uses the **TempActiveRef12** function to select cells A105:C110.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveRefExample(void)
{
    Excel12f(xlcSelect, 0, 1, TempActiveRef12(104, 109, 0, 2));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="4153a-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4153a-128">See also</span></span>



[<span data-ttu-id="4153a-129">Fonctions de la bibliothèque Framework</span><span class="sxs-lookup"><span data-stu-id="4153a-129">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

