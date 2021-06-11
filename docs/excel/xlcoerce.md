---
title: xlCoerce
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlCoerce
keywords:
- fonction xeuseerce [excel 2007]
localization_priority: Normal
ms.assetid: 9d47c16c-a7e7-4998-b594-9cf001827b7b
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d84839535d5eb913ca8a62d631238e3330683d0e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424832"
---
# <a name="xlcoerce"></a><span data-ttu-id="52516-104">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="52516-104">xlCoerce</span></span>

 <span data-ttu-id="52516-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="52516-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="52516-106">Convertit un type de **XLOPER** /  **XLOPER12** en un autre ou recherche des valeurs de cellule sur une feuille.</span><span class="sxs-lookup"><span data-stu-id="52516-106">Converts one type of **XLOPER**/ **XLOPER12** to another, or looks up cell values on a sheet.</span></span> 
  
```cs
Excel12(xlCoerce, LPXLOPER12 pxRes, 2, LPXLOPER12 pxSource, LPXLOPER12 pxDestType);
```

## <a name="parameters"></a><span data-ttu-id="52516-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="52516-107">Parameters</span></span>

 <span data-ttu-id="52516-108">_pxSource_</span><span class="sxs-lookup"><span data-stu-id="52516-108">_pxSource_</span></span>
  
<span data-ttu-id="52516-109">XlOPER  /  **XLOPER12** source à convertir.</span><span class="sxs-lookup"><span data-stu-id="52516-109">The source **XLOPER**/ **XLOPER12** that needs to be converted.</span></span> 
  
 <span data-ttu-id="52516-110">_pxDestType_ (**xltypeInt**)</span><span class="sxs-lookup"><span data-stu-id="52516-110">_pxDestType_ (**xltypeInt**)</span></span>
  
<span data-ttu-id="52516-111">(Facultatif).</span><span class="sxs-lookup"><span data-stu-id="52516-111">(Optional).</span></span> <span data-ttu-id="52516-112">Masque de bits des types résultants que vous êtes prêt à accepter.</span><span class="sxs-lookup"><span data-stu-id="52516-112">A bit-mask of the resulting types you are willing to accept.</span></span> <span data-ttu-id="52516-113">Vous devez utiliser l’opérateur **OR** au niveau du bit ( | ) pour spécifier plusieurs types possibles.</span><span class="sxs-lookup"><span data-stu-id="52516-113">You should use the bitwise **OR** operator ( | ) to specify multiple possible types.</span></span> <span data-ttu-id="52516-114">Si cet argument est omis, les références à des cellules individuelles sont converties en un des types de valeur **xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil** (si la cellule référencé est vide) et les références aux blocs de cellules sont converties en **xltypeMulti**.</span><span class="sxs-lookup"><span data-stu-id="52516-114">If this argument is omitted, references to single cells are converted to one of the value types **xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil** (if the referred-to cell is empty), and references to blocks of cells are converted to **xltypeMulti**.</span></span> <span data-ttu-id="52516-115">Cela rend **xlCoerce** le moyen le plus pratique de rechercher des valeurs de cellule.</span><span class="sxs-lookup"><span data-stu-id="52516-115">This makes **xlCoerce** the most convenient way to look up cell values.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="52516-116">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="52516-116">Property value/Return value</span></span>

<span data-ttu-id="52516-117">Renvoie la valeur contrainte (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil** ou **xltypeMulti**).</span><span class="sxs-lookup"><span data-stu-id="52516-117">Returns the coerced value (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil**, or **xltypeMulti**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="52516-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="52516-118">Remarks</span></span>

 <span data-ttu-id="52516-119">**xlCoerce ne peut** pas convertir vers ou à partir **de xltypeBigData** ou **xltypeFlow**.</span><span class="sxs-lookup"><span data-stu-id="52516-119">**xlCoerce** cannot convert to or from **xltypeBigData** or **xltypeFlow**.</span></span> <span data-ttu-id="52516-120">Passer un type **xltypeMissing** ou **xltypeNil** en tant que  _pxDestType_ équivaut à omettre l’argument.</span><span class="sxs-lookup"><span data-stu-id="52516-120">Passing an **xltypeMissing** or **xltypeNil** type as  _pxDestType_ is equivalent to omitting the argument.</span></span> <span data-ttu-id="52516-121">La conversion peut échouer dans certains cas.</span><span class="sxs-lookup"><span data-stu-id="52516-121">Conversion can fail in some cases.</span></span> <span data-ttu-id="52516-122">Par exemple, certaines chaînes ne peuvent pas être converties en nombres, tandis que d’autres le peuvent.</span><span class="sxs-lookup"><span data-stu-id="52516-122">For example, some strings cannot be converted to numbers, whereas others can.</span></span> 
  
<span data-ttu-id="52516-123">Si un tableau ou une référence à plusieurs cellules est converti en un seul type de valeur, le résultat est la valeur de la cellule supérieure gauche ou de l’élément de tableau.</span><span class="sxs-lookup"><span data-stu-id="52516-123">If an array or a multi-cell reference is converted to a single value type, the result is the value of the top left cell or array element.</span></span>
  
## <a name="example"></a><span data-ttu-id="52516-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="52516-124">Example</span></span>

<span data-ttu-id="52516-125">Le code suivant se trouve dans  `\SAMPLES\EXAMPLE\EXAMPLE.C` .</span><span class="sxs-lookup"><span data-stu-id="52516-125">The following code can be found in  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="52516-126">La fonction **xlcAlert** tente implicitement de convertir son argument en chaîne afin que l’étape de contrainte indiquée ici puisse en fait être supprimée et **que xInt** soit transmis directement à **xlcAlert**.</span><span class="sxs-lookup"><span data-stu-id="52516-126">The **xlcAlert** function implicitly tries to convert its argument to a string so that the coercion step shown here could in fact be removed, and **xInt** could be passed directly to **xlcAlert**.</span></span> <span data-ttu-id="52516-127">Comme **xlcAlert est** une macro de commande, ce code ne fonctionne correctement qu’en cas d’appel à partir d’une feuille macro.</span><span class="sxs-lookup"><span data-stu-id="52516-127">As **xlcAlert** is a command macro, this code only works correctly when called from a macro sheet.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="52516-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52516-128">See also</span></span>



[<span data-ttu-id="52516-129">xlSet</span><span class="sxs-lookup"><span data-stu-id="52516-129">xlSet</span></span>](xlset.md)


[<span data-ttu-id="52516-130">Fonctions de l’API C à appeler à partir d’un fichier DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="52516-130">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

