---
title: xlCoerce
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlCoerce
keywords:
- fonction xlCoerce [Excel 2007]
localization_priority: Normal
ms.assetid: 9d47c16c-a7e7-4998-b594-9cf001827b7b
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: d84839535d5eb913ca8a62d631238e3330683d0e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303961"
---
# <a name="xlcoerce"></a><span data-ttu-id="dfdfc-104">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="dfdfc-104">xlCoerce</span></span>

 <span data-ttu-id="dfdfc-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="dfdfc-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="dfdfc-106">Convertit un type de**XLOPER12** de type **XLOPER**/ en un autre, ou recherche des valeurs de cellule dans une feuille.</span><span class="sxs-lookup"><span data-stu-id="dfdfc-106">Converts one type of **XLOPER**/ **XLOPER12** to another, or looks up cell values on a sheet.</span></span> 
  
```cs
Excel12(xlCoerce, LPXLOPER12 pxRes, 2, LPXLOPER12 pxSource, LPXLOPER12 pxDestType);
```

## <a name="parameters"></a><span data-ttu-id="dfdfc-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dfdfc-107">Parameters</span></span>

 <span data-ttu-id="dfdfc-108">_pxSource_</span><span class="sxs-lookup"><span data-stu-id="dfdfc-108">_pxSource_</span></span>
  
<span data-ttu-id="dfdfc-109">La source **XLOPER**/ \*\*\*\* source doit être convertie.</span><span class="sxs-lookup"><span data-stu-id="dfdfc-109">The source **XLOPER**/ **XLOPER12** that needs to be converted.</span></span> 
  
 <span data-ttu-id="dfdfc-110">_pxDestType_ (**xltypeInt**)</span><span class="sxs-lookup"><span data-stu-id="dfdfc-110">_pxDestType_ (**xltypeInt**)</span></span>
  
<span data-ttu-id="dfdfc-111">(Facultatif).</span><span class="sxs-lookup"><span data-stu-id="dfdfc-111">(Optional).</span></span> <span data-ttu-id="dfdfc-112">Masque de bits des types résultants que vous êtes prêt à accepter.</span><span class="sxs-lookup"><span data-stu-id="dfdfc-112">A bit-mask of the resulting types you are willing to accept.</span></span> <span data-ttu-id="dfdfc-113">Vous devez utiliser l'opérateur \*\*\*\* or au niveau du bit (|) pour spécifier plusieurs types possibles.</span><span class="sxs-lookup"><span data-stu-id="dfdfc-113">You should use the bitwise **OR** operator ( | ) to specify multiple possible types.</span></span> <span data-ttu-id="dfdfc-114">Si vous ne spécifiez pas cet argument, les références à des cellules uniques sont converties en l'un des types de valeur **xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil** (si la cellule référencée est vide) et des références à des blocs de cellules sont converties en **xltypeMulti**.</span><span class="sxs-lookup"><span data-stu-id="dfdfc-114">If this argument is omitted, references to single cells are converted to one of the value types **xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil** (if the referred-to cell is empty), and references to blocks of cells are converted to **xltypeMulti**.</span></span> <span data-ttu-id="dfdfc-115">Cela rend **xlCoerce** le moyen le plus commode de rechercher des valeurs de cellule.</span><span class="sxs-lookup"><span data-stu-id="dfdfc-115">This makes **xlCoerce** the most convenient way to look up cell values.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="dfdfc-116">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="dfdfc-116">Property value/Return value</span></span>

<span data-ttu-id="dfdfc-117">Renvoie la valeur forcée (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil**ou **xltypeMulti**).</span><span class="sxs-lookup"><span data-stu-id="dfdfc-117">Returns the coerced value (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil**, or **xltypeMulti**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dfdfc-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="dfdfc-118">Remarks</span></span>

 <span data-ttu-id="dfdfc-119">**xlCoerce** ne peut pas convertir vers ou à partir de **xltypeBigData** ou **xltypeFlow**.</span><span class="sxs-lookup"><span data-stu-id="dfdfc-119">**xlCoerce** cannot convert to or from **xltypeBigData** or **xltypeFlow**.</span></span> <span data-ttu-id="dfdfc-120">Le passage d'un type **xltypeMissing** ou **xltypeNil** en tant que _pxDestType_ revient à omettre l'argument.</span><span class="sxs-lookup"><span data-stu-id="dfdfc-120">Passing an **xltypeMissing** or **xltypeNil** type as  _pxDestType_ is equivalent to omitting the argument.</span></span> <span data-ttu-id="dfdfc-121">Dans certains cas, la conversion peut échouer.</span><span class="sxs-lookup"><span data-stu-id="dfdfc-121">Conversion can fail in some cases.</span></span> <span data-ttu-id="dfdfc-122">Par exemple, certaines chaînes ne peuvent pas être converties en nombres, contrairement à d'autres.</span><span class="sxs-lookup"><span data-stu-id="dfdfc-122">For example, some strings cannot be converted to numbers, whereas others can.</span></span> 
  
<span data-ttu-id="dfdfc-123">Si un tableau ou une référence à plusieurs cellules est convertie en un seul type valeur, le résultat est la valeur de la cellule supérieure gauche ou du tableau.</span><span class="sxs-lookup"><span data-stu-id="dfdfc-123">If an array or a multi-cell reference is converted to a single value type, the result is the value of the top left cell or array element.</span></span>
  
## <a name="example"></a><span data-ttu-id="dfdfc-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="dfdfc-124">Example</span></span>

<span data-ttu-id="dfdfc-125">Le code suivant est disponible dans `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="dfdfc-125">The following code can be found in  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="dfdfc-126">La fonction **xlcAlert** tente implicitement de convertir son argument en une chaîne de façon à ce que l'étape de forçage indiquée ici puisse être supprimée et **xInt** puisse être passé directement à **xlcAlert**.</span><span class="sxs-lookup"><span data-stu-id="dfdfc-126">The **xlcAlert** function implicitly tries to convert its argument to a string so that the coercion step shown here could in fact be removed, and **xInt** could be passed directly to **xlcAlert**.</span></span> <span data-ttu-id="dfdfc-127">Comme **xlcAlert** est une macro de commande, ce code fonctionne uniquement lorsqu'il est appelé à partir d'une feuille macro.</span><span class="sxs-lookup"><span data-stu-id="dfdfc-127">As **xlcAlert** is a command macro, this code only works correctly when called from a macro sheet.</span></span> 
  
```cs
short WINAPI xlCoerceExample(short iVal)
{
   XLOPER12 xStr, xInt, xDestType;
   xInt.xltype = xltypeInt;
   xInt.val.w = iVal;
   xDestType.xltype = xltypeInt;
   xDestType.val.w = xltypeStr;
   Excel12f(xlCoerce, &xStr, 2, (LPXLOPER12)&xInt, (LPXLOPER12)&xDestType);
   Excel12f(xlcAlert, 0, 1, (LPXLOPER12)&xStr);
   Excel12f(xlFree, 0, 1, (LPXLOPER12)&xStr);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="dfdfc-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dfdfc-128">See also</span></span>



[<span data-ttu-id="dfdfc-129">xlSet</span><span class="sxs-lookup"><span data-stu-id="dfdfc-129">xlSet</span></span>](xlset.md)


[<span data-ttu-id="dfdfc-130">Fonctions de l’API C à appeler à partir d’un fichier DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="dfdfc-130">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

