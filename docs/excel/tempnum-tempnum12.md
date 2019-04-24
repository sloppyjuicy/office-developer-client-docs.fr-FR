---
title: TempNum/TempNum12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempNum
- TempNum12
keywords:
- fonction tempnum12 [Excel 2007], fonction TempNum [Excel 2007]
localization_priority: Normal
ms.assetid: 5b74d618-db3a-4d84-bd17-4fee7ae3b51e
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: cabd44ab828a2cfe22253e9aaf12abf7b7709d69
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310359"
---
# <a name="tempnumtempnum12"></a><span data-ttu-id="5bb5d-104">TempNum/TempNum12</span><span class="sxs-lookup"><span data-stu-id="5bb5d-104">TempNum/TempNum12</span></span>

 <span data-ttu-id="5bb5d-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5bb5d-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="5bb5d-106">Fonction de bibliothèque d'infrastructure qui crée une expression **XLOPER**/ \*\*\*\* temporaire contenant un numéro de feuille de calcul Microsoft Excel (un type IEEE de 8 octets).</span><span class="sxs-lookup"><span data-stu-id="5bb5d-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing a Microsoft Excel worksheet number (an IEEE 8-byte double).</span></span> 
  
```cs
LPXLOPER TempNum(double d);
LPXLOPER12 TempNum12(double d);
```

## <a name="parameters"></a><span data-ttu-id="5bb5d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5bb5d-107">Parameters</span></span>

 <span data-ttu-id="5bb5d-108">_d_ (**double**)</span><span class="sxs-lookup"><span data-stu-id="5bb5d-108">_d_ (**double**)</span></span>
  
<span data-ttu-id="5bb5d-109">Valeur prévue.</span><span class="sxs-lookup"><span data-stu-id="5bb5d-109">The intended value.</span></span> <span data-ttu-id="5bb5d-110">Notez que les numéros IEEE sous-normaux ne sont actuellement pas pris en charge et arrondis à zéro.</span><span class="sxs-lookup"><span data-stu-id="5bb5d-110">Note that IEEE sub-normal numbers are not currently supported and are rounded to zero.</span></span> <span data-ttu-id="5bb5d-111">L'infini négatif est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="5bb5d-111">Negative infinity is supported.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="5bb5d-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5bb5d-112">Return value</span></span>

<span data-ttu-id="5bb5d-113">Renvoie un **xltypeNum** numérique contenant la valeur transmise ou zéro si la valeur passée est Sub-normal.</span><span class="sxs-lookup"><span data-stu-id="5bb5d-113">Returns a numeric **xltypeNum** containing the value passed in or zero if the passed in value was sub-normal.</span></span> 
  
## <a name="example"></a><span data-ttu-id="5bb5d-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="5bb5d-114">Example</span></span>

<span data-ttu-id="5bb5d-115">Cet exemple utilise la fonction **TempNum12** pour transmettre un argument à **xlfGetWorkspace**.</span><span class="sxs-lookup"><span data-stu-id="5bb5d-115">This example uses the **TempNum12** function to pass an argument to **xlfGetWorkspace**.</span></span>
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempNumExample(void)
{
   XLOPER12 xRes;
   Excel12f(xlfGetWorkspace, &xRes, 1, TempNum12(44));
   Excel12f(xlFree, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="5bb5d-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5bb5d-116">See also</span></span>



[<span data-ttu-id="5bb5d-117">Fonctions de la bibliothèque Framework</span><span class="sxs-lookup"><span data-stu-id="5bb5d-117">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

