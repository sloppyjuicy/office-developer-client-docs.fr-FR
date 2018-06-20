---
title: xlCoerce
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlCoerce
keywords:
- fonction xlCoerce [excel 2007]
localization_priority: Normal
ms.assetid: 9d47c16c-a7e7-4998-b594-9cf001827b7b
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e0474b81a6d24663fe85303efc8fe2fd62cfdd82
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782222"
---
# <a name="xlcoerce"></a><span data-ttu-id="57ee1-104">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="57ee1-104">xlCoerce</span></span>

 <span data-ttu-id="57ee1-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="57ee1-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="57ee1-106">Convertit un type de **XLOPER**/ **XLOPER12** vers un autre, ou recherche des valeurs de cellule dans une feuille.</span><span class="sxs-lookup"><span data-stu-id="57ee1-106">Converts one type of **XLOPER**/ **XLOPER12** to another, or looks up cell values on a sheet.</span></span> 
  
```cs
Excel12(xlCoerce, LPXLOPER12 pxRes, 2, LPXLOPER12 pxSource, LPXLOPER12 pxDestType);
```

## <a name="parameters"></a><span data-ttu-id="57ee1-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="57ee1-107">Parameters</span></span>

 <span data-ttu-id="57ee1-108">_pxSource_</span><span class="sxs-lookup"><span data-stu-id="57ee1-108">_pxSource_</span></span>
  
<span data-ttu-id="57ee1-109">La source **XLOPER**/ **XLOPER12** qui doit être convertie.</span><span class="sxs-lookup"><span data-stu-id="57ee1-109">The source **XLOPER**/ **XLOPER12** that needs to be converted.</span></span> 
  
 <span data-ttu-id="57ee1-110">_pxDestType_ (**xltypeInt**)</span><span class="sxs-lookup"><span data-stu-id="57ee1-110">_pxDestType_ (**xltypeInt**)</span></span>
  
<span data-ttu-id="57ee1-111">(Facultatif).</span><span class="sxs-lookup"><span data-stu-id="57ee1-111">(Optional).</span></span> <span data-ttu-id="57ee1-112">Un masque de bits des types qui en résulte, vous êtes prêt à accepter.</span><span class="sxs-lookup"><span data-stu-id="57ee1-112">A bit-mask of the resulting types you are willing to accept.</span></span> <span data-ttu-id="57ee1-113">Vous devez utiliser l’opérateur de bits **OR** (|) pour spécifier plusieurs types possibles.</span><span class="sxs-lookup"><span data-stu-id="57ee1-113">You should use the bitwise **OR** operator ( | ) to specify multiple possible types.</span></span> <span data-ttu-id="57ee1-114">Si cet argument est omis, les références à des cellules uniques sont convertis à un des types de valeur **xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil** (si la cellule référencée est vide) et références aux blocs des cellules sont converties en **xltypeMulti**.</span><span class="sxs-lookup"><span data-stu-id="57ee1-114">If this argument is omitted, references to single cells are converted to one of the value types **xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil** (if the referred-to cell is empty), and references to blocks of cells are converted to **xltypeMulti**.</span></span> <span data-ttu-id="57ee1-115">Cela rend **xlCoerce** le meilleur moyen de rechercher des valeurs de cellules.</span><span class="sxs-lookup"><span data-stu-id="57ee1-115">This makes **xlCoerce** the most convenient way to look up cell values.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="57ee1-116">Propriété valeur/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="57ee1-116">Property value/Return value</span></span>

<span data-ttu-id="57ee1-117">Renvoie la valeur forcée (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil**ou **xltypeMulti**).</span><span class="sxs-lookup"><span data-stu-id="57ee1-117">Returns the coerced value (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil**, or **xltypeMulti**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="57ee1-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="57ee1-118">Remarks</span></span>

 <span data-ttu-id="57ee1-119">Impossible de convertir **xlCoerce** vers ou depuis **xltypeBigData** ou **xltypeFlow**.</span><span class="sxs-lookup"><span data-stu-id="57ee1-119">**xlCoerce** cannot convert to or from **xltypeBigData** or **xltypeFlow**.</span></span> <span data-ttu-id="57ee1-120">En passant un type **xltypeMissing** ou **xltypeNil** comme _pxDestType_ équivaut à omettre l’argument.</span><span class="sxs-lookup"><span data-stu-id="57ee1-120">Passing an **xltypeMissing** or **xltypeNil** type as  _pxDestType_ is equivalent to omitting the argument.</span></span> <span data-ttu-id="57ee1-121">Conversion peut échouer dans certains cas.</span><span class="sxs-lookup"><span data-stu-id="57ee1-121">Conversion can fail in some cases.</span></span> <span data-ttu-id="57ee1-122">Par exemple, certaines chaînes ne peuvent pas être converties en nombres, tandis que d’autres personnes peuvent.</span><span class="sxs-lookup"><span data-stu-id="57ee1-122">For example, some strings cannot be converted to numbers, whereas others can.</span></span> 
  
<span data-ttu-id="57ee1-123">Si une matrice ou une référence de cellule multiples est convertie en un type de valeur de type single, le résultat est la valeur de l’élément supérieur gauche cellule ou un tableau.</span><span class="sxs-lookup"><span data-stu-id="57ee1-123">If an array or a multi-cell reference is converted to a single value type, the result is the value of the top left cell or array element.</span></span>
  
## <a name="example"></a><span data-ttu-id="57ee1-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="57ee1-124">Example</span></span>

<span data-ttu-id="57ee1-125">Vous trouverez le code suivant dans `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="57ee1-125">The following code can be found in  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="57ee1-126">La fonction **xlcAlert** implicitement tente de convertir une chaîne de son argument afin que l’étape du forçage de type indiqué ici en fait pu être supprimé, et **xInt** peut être passé directement à **xlcAlert**.</span><span class="sxs-lookup"><span data-stu-id="57ee1-126">The **xlcAlert** function implicitly tries to convert its argument to a string so that the coercion step shown here could in fact be removed, and **xInt** could be passed directly to **xlcAlert**.</span></span> <span data-ttu-id="57ee1-127">**XlcAlert** est une macro de commande, ce code ne fonctionne correctement lorsqu’elle est appelée à partir d’une feuille macro.</span><span class="sxs-lookup"><span data-stu-id="57ee1-127">As **xlcAlert** is a command macro, this code only works correctly when called from a macro sheet.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="57ee1-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57ee1-128">See also</span></span>



[<span data-ttu-id="57ee1-129">xlSet</span><span class="sxs-lookup"><span data-stu-id="57ee1-129">xlSet</span></span>](xlset.md)


[<span data-ttu-id="57ee1-130">Fonctions de l’API C qui peuvent être appelées uniquement à partir d’une DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="57ee1-130">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

