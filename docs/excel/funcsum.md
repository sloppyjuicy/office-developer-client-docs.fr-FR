---
title: FuncSum
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncSum
keywords:
- fonction funcsum [excel 2007]
localization_priority: Normal
ms.assetid: 934192ef-8a89-4dbb-bd37-01e92ba24256
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 14db5812165812161cf7031f75338a981251dfd2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406940"
---
# <a name="funcsum"></a><span data-ttu-id="663c8-104">FuncSum</span><span class="sxs-lookup"><span data-stu-id="663c8-104">FuncSum</span></span>

 <span data-ttu-id="663c8-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="663c8-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="663c8-106">Exemple de fonction de feuille de calcul définie par l’utilisateur qui prend 1 à 29 arguments et calcule leur somme.</span><span class="sxs-lookup"><span data-stu-id="663c8-106">Example user-defined worksheet function that takes 1 to 29 arguments and computes their sum.</span></span> <span data-ttu-id="663c8-107">Chaque argument peut être un nombre unique, une plage ou un tableau.</span><span class="sxs-lookup"><span data-stu-id="663c8-107">Each argument can be a single number, a range, or an array.</span></span> <span data-ttu-id="663c8-108">Lorsque GENERIC.xll est chargé, il inscrit cette fonction afin qu’elle puisse être appelée à partir de la feuille de calcul.</span><span class="sxs-lookup"><span data-stu-id="663c8-108">When GENERIC.xll is loaded, it registers this function so that it can be called from the worksheet.</span></span> 
  
```cs
LPXLOPER12 WINAPI FuncSum(LPXLOPER12 px1, LPXLOPER12 px2, LPXLOPER12 px3,LPXLOPER12 px4, LPXLOPER12 px5, LPXLOPER12 px6, LPXLOPER12 px7,LPXLOPER12 px8, LPXLOPER12 px9, LPXLOPER12 px10, LPXLOPER12 px11,LPXLOPER12 px12, LPXLOPER12 px13, LPXLOPER12 px14, LPXLOPER12 px15,LPXLOPER12 px16, LPXLOPER12 px17, LPXLOPER12 px18, LPXLOPER12 px19,LPXLOPER12 px20, LPXLOPER12 px21, LPXLOPER12 px22, LPXLOPER12 px23,LPXLOPER12 px24, LPXLOPER12 px25, LPXLOPER12 px26, LPXLOPER12 px27,LPXLOPER12 px28, LPXLOPER12 px29);
```

## <a name="parameters"></a><span data-ttu-id="663c8-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="663c8-109">Parameters</span></span>

 <span data-ttu-id="663c8-110">_px1-px29_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="663c8-110">_px1-px29_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="663c8-111">Pointeurs vers les arguments **XLOPER12.**</span><span class="sxs-lookup"><span data-stu-id="663c8-111">Pointers to **XLOPER12** arguments.</span></span> <span data-ttu-id="663c8-112">La fonction accepte n’importe quel type d’entrée, mais elle est codée uniquement pour fonctionner sur des nombres, des tableaux littéraux de nombres et des plages contenant uniquement des nombres ou des cellules vides.</span><span class="sxs-lookup"><span data-stu-id="663c8-112">The function accepts any kind of input type but is coded only to operate on numbers, literal arrays of numbers, and ranges containing only numbers or blank cells.</span></span> <span data-ttu-id="663c8-113">Si moins de 29 arguments sont fournis, les arguments restants sont fournis sous la forme **xltypeMissing**.</span><span class="sxs-lookup"><span data-stu-id="663c8-113">If fewer than 29 arguments are supplied, the remaining arguments are supplied as **xltypeMissing**.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="663c8-114">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="663c8-114">Property value/Return value</span></span>

<span data-ttu-id="663c8-115">(**LPXLOPER12 xltypeNum** ou **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="663c8-115">(**LPXLOPER12 xltypeNum** or **xltypeErr**)</span></span>
  
<span data-ttu-id="663c8-116">Somme des arguments ou des #VALUE!</span><span class="sxs-lookup"><span data-stu-id="663c8-116">The sum of the arguments or #VALUE!</span></span> <span data-ttu-id="663c8-117">s’il existe des nombres non numériques dans la liste d’arguments fournie ou dans une cellule d’une plage ou d’un élément dans un tableau.</span><span class="sxs-lookup"><span data-stu-id="663c8-117">if there are non-numerics in the supplied argument list or in a cell in a range or element in an array.</span></span>
  
### <a name="example"></a><span data-ttu-id="663c8-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="663c8-118">Example</span></span>

<span data-ttu-id="663c8-119">Voir  `\SAMPLES\GENERIC\GENERIC.C` le code source pour cette fonction.</span><span class="sxs-lookup"><span data-stu-id="663c8-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="663c8-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="663c8-120">See also</span></span>



[<span data-ttu-id="663c8-121">Fonctions dans le fichier DLL générique</span><span class="sxs-lookup"><span data-stu-id="663c8-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

