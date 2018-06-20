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
- fonction tempnum12 [excel 2007], fonction TempNum [Excel 2007]
localization_priority: Normal
ms.assetid: 5b74d618-db3a-4d84-bd17-4fee7ae3b51e
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 5ebe58dba32c2cf0382bf0811713eaa0a5471dda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782195"
---
# <a name="tempnumtempnum12"></a><span data-ttu-id="d3bb1-104">TempNum/TempNum12</span><span class="sxs-lookup"><span data-stu-id="d3bb1-104">TempNum/TempNum12</span></span>

 <span data-ttu-id="d3bb1-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d3bb1-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d3bb1-106">Fonction de bibliothèque Framework crée un temporaire **XLOPER**/ **XLOPER12** contenant un numéro de feuille de calcul Microsoft Excel (un double de 8 octets IEEE).</span><span class="sxs-lookup"><span data-stu-id="d3bb1-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing a Microsoft Excel worksheet number (an IEEE 8-byte double).</span></span> 
  
```cs
LPXLOPER TempNum(double d);
LPXLOPER12 TempNum12(double d);
```

## <a name="parameters"></a><span data-ttu-id="d3bb1-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d3bb1-107">Parameters</span></span>

 <span data-ttu-id="d3bb1-108">_d_ (**double**)</span><span class="sxs-lookup"><span data-stu-id="d3bb1-108">_d_ (**double**)</span></span>
  
<span data-ttu-id="d3bb1-109">La valeur attendue.</span><span class="sxs-lookup"><span data-stu-id="d3bb1-109">The intended value.</span></span> <span data-ttu-id="d3bb1-110">Notez que les numéros sous-fonctionnalités normales IEEE ne sont pas actuellement pris en charge et sont arrondies à zéro.</span><span class="sxs-lookup"><span data-stu-id="d3bb1-110">Note that IEEE sub-normal numbers are not currently supported and are rounded to zero.</span></span> <span data-ttu-id="d3bb1-111">L’infini négatif est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d3bb1-111">Negative infinity is supported.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="d3bb1-112">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="d3bb1-112">Return value</span></span>

<span data-ttu-id="d3bb1-113">Renvoie un numérique **xltypeNum** contenant la valeur passé ou zéro si la valeur passée était sous-fonctionnalités normale.</span><span class="sxs-lookup"><span data-stu-id="d3bb1-113">Returns a numeric **xltypeNum** containing the value passed in or zero if the passed in value was sub-normal.</span></span> 
  
## <a name="example"></a><span data-ttu-id="d3bb1-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="d3bb1-114">Example</span></span>

<span data-ttu-id="d3bb1-115">Cet exemple utilise la fonction **TempNum12** pour passer un argument à **xlfGetWorkspace**.</span><span class="sxs-lookup"><span data-stu-id="d3bb1-115">This example uses the **TempNum12** function to pass an argument to **xlfGetWorkspace**.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="d3bb1-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d3bb1-116">See also</span></span>



[<span data-ttu-id="d3bb1-117">Fonctions de la bibliothèque Framework</span><span class="sxs-lookup"><span data-stu-id="d3bb1-117">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

