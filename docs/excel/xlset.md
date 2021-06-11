---
title: xlSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSet
keywords:
- fonction xlset [excel 2007]
localization_priority: Normal
ms.assetid: 121e6212-0692-4430-97be-4792b53719bf
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 0912c1d40882933778d0df927ceb9de773063444
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404602"
---
# <a name="xlset"></a><span data-ttu-id="94d21-104">xlSet</span><span class="sxs-lookup"><span data-stu-id="94d21-104">xlSet</span></span>

<span data-ttu-id="94d21-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="94d21-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="94d21-106">Place très rapidement des valeurs constantes dans des cellules ou des plages.</span><span class="sxs-lookup"><span data-stu-id="94d21-106">Puts constant values into cells or ranges very quickly.</span></span> <span data-ttu-id="94d21-107">Pour plus d’informations, voir « xlSet et workbooks with Array Formulas » dans [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="94d21-107">For more information, see "xlSet and Workbooks with Array Formulas" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel12(xlSet, LPXLOPER12 pxRes, 2, LPXLOPER12 pxReference, LPXLOPER pxValue);
```

## <a name="parameters"></a><span data-ttu-id="94d21-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="94d21-108">Parameters</span></span>

<span data-ttu-id="94d21-109">_pxReference_ (**xltypeRef** ou **xltypeSRef**)</span><span class="sxs-lookup"><span data-stu-id="94d21-109">_pxReference_ (**xltypeRef** or **xltypeSRef**)</span></span>
  
<span data-ttu-id="94d21-110">Référence rectangulaire décrivant la ou les cellules cibles.</span><span class="sxs-lookup"><span data-stu-id="94d21-110">A rectangular reference describing the target cell or cells.</span></span> <span data-ttu-id="94d21-111">La référence doit décrire les cellules adjacentes, de sorte que dans un **xltypeRef** `val.mref.lpmref->count` doit être définie sur 1.</span><span class="sxs-lookup"><span data-stu-id="94d21-111">The reference must describe adjacent cells, so that in an **xltypeRef** `val.mref.lpmref->count` must be set to 1.</span></span> 
  
<span data-ttu-id="94d21-112">_pxValue_</span><span class="sxs-lookup"><span data-stu-id="94d21-112">_pxValue_</span></span>
  
<span data-ttu-id="94d21-113">Valeur ou valeur à placer dans la ou les cellules.</span><span class="sxs-lookup"><span data-stu-id="94d21-113">The value or values to be placed into the cell or cells.</span></span> <span data-ttu-id="94d21-114">Pour plus d’informations, voir la section « Remarques ».</span><span class="sxs-lookup"><span data-stu-id="94d21-114">For more information, see the "Remarks" section.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="94d21-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="94d21-115">Remarks</span></span>

### <a name="pxvalue-argument"></a><span data-ttu-id="94d21-116">Argument pxValue</span><span class="sxs-lookup"><span data-stu-id="94d21-116">pxValue argument</span></span>

<span data-ttu-id="94d21-117">_pxValue peut_ être une valeur ou un tableau.</span><span class="sxs-lookup"><span data-stu-id="94d21-117">_pxValue_ can either be a value or an array.</span></span> <span data-ttu-id="94d21-118">S’il s’agit d’une valeur, la plage de destination entière est remplie avec cette valeur.</span><span class="sxs-lookup"><span data-stu-id="94d21-118">If it is a value, the entire destination range is filled with that value.</span></span> <span data-ttu-id="94d21-119">S’il s’agit d’un tableau (**xltypeMulti**), les éléments du tableau sont placés aux emplacements correspondants dans le rectangle.</span><span class="sxs-lookup"><span data-stu-id="94d21-119">If it is an array (**xltypeMulti**), the elements of the array are put into the corresponding locations in the rectangle.</span></span>
  
<span data-ttu-id="94d21-120">Si vous utilisez un tableau horizontal pour le deuxième argument, il est dupliqué vers le bas pour remplir le rectangle entier.</span><span class="sxs-lookup"><span data-stu-id="94d21-120">If you use a horizontal array for the second argument, it is duplicated down to fill the entire rectangle.</span></span> <span data-ttu-id="94d21-121">Si vous utilisez un tableau vertical, il est dupliqué à droite pour remplir le rectangle entier.</span><span class="sxs-lookup"><span data-stu-id="94d21-121">If you use a vertical array, it is duplicated right to fill the entire rectangle.</span></span> <span data-ttu-id="94d21-122">Si vous utilisez un tableau rectangulaire et qu’il est trop petit pour la plage rectangulaire que vous souhaitez y placer, cette plage est ajoutée avec **#N/A.**</span><span class="sxs-lookup"><span data-stu-id="94d21-122">If you use a rectangular array, and it is too small for the rectangular range you want to put it in, that range is padded with **#N/A** s.</span></span>
  
<span data-ttu-id="94d21-123">Si la plage cible est plus petite que le tableau source, les valeurs sont copiées dans les limites de la plage cible et les données supplémentaires sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="94d21-123">If the target range is smaller than the source array, the values are copied in up to the limits of the target range and the extra data are ignored.</span></span>
  
<span data-ttu-id="94d21-124">Pour effacer un élément du rectangle de destination, utilisez un élément de tableau de type **xltypeNil** dans le tableau source.</span><span class="sxs-lookup"><span data-stu-id="94d21-124">To clear an element of the destination rectangle, use an **xltypeNil** type array element in the source array.</span></span> <span data-ttu-id="94d21-125">Pour effacer l’intégralité du rectangle de destination, omettez le deuxième argument.</span><span class="sxs-lookup"><span data-stu-id="94d21-125">To clear the entire destination rectangle, omit the second argument.</span></span> 
  
### <a name="restrictions"></a><span data-ttu-id="94d21-126">Restrictions</span><span class="sxs-lookup"><span data-stu-id="94d21-126">Restrictions</span></span>

<span data-ttu-id="94d21-127">**XlSet ne** peut pas être annulé.</span><span class="sxs-lookup"><span data-stu-id="94d21-127">**xlSet** cannot be undone.</span></span> <span data-ttu-id="94d21-128">En outre, il détruit toutes les informations d’annuler qui auraient pu être disponibles auparavant.</span><span class="sxs-lookup"><span data-stu-id="94d21-128">In addition, it destroys any undo information that may have been available before.</span></span> 
  
<span data-ttu-id="94d21-129">**XlSet peut** placer uniquement des constantes, et non des formules, dans les cellules.</span><span class="sxs-lookup"><span data-stu-id="94d21-129">**xlSet** can put only constants, not formulas, into cells.</span></span> 
  
<span data-ttu-id="94d21-130">**XlSet se** comporte comme une fonction équivalente à une commande de classe 3 ; autrement dit, elle est disponible uniquement à l’intérieur d’une DLL lorsque la DLL  est appelée à partir d’un  objet, d’une macro, d’un menu, d’une barre d’outils, d’une touche de raccourci ou du bouton Exécuter dans la boîte de dialogue **Macro** (accessible à partir de l’onglet Affichage du ruban à partir de Excel 2007 et du **menu** Outils dans les versions antérieures).</span><span class="sxs-lookup"><span data-stu-id="94d21-130">**xlSet** behaves as a Class 3 command-equivalent function; that is, it is available only inside a DLL when the DLL is called from an object, macro, menu, toolbar, shortcut key, or the **Run** button in the **Macro** dialog box (accessed from **View** tab on the ribbon starting in Excel 2007, and the **Tools** menu in earlier versions).</span></span> 
  
## <a name="example"></a><span data-ttu-id="94d21-131">Exemple</span><span class="sxs-lookup"><span data-stu-id="94d21-131">Example</span></span>

<span data-ttu-id="94d21-132">L’exemple suivant remplit B205:B206 avec la valeur transmise à partir d’une macro.</span><span class="sxs-lookup"><span data-stu-id="94d21-132">The following example fills B205:B206 with the value that was passed in from a macro.</span></span> <span data-ttu-id="94d21-133">Cet exemple de fonction de commande nécessite un argument et fonctionne uniquement s’il est appelé à partir d’une feuille macro XLM ou d’un module VBA à l’aide de la méthode **Application.Run.**</span><span class="sxs-lookup"><span data-stu-id="94d21-133">This command function example requires an argument, and so will only work if called from an XLM macro sheet, or from a VBA module using the **Application.Run** method.</span></span> 
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlSetExample(short int iVal)
{
   XLOPER12 xRef, xValue;
   xRef.xltype = xltypeSRef;
   xRef.val.sref.count = 1;
   xRef.val.sref.ref.rwFirst = 204;
   xRef.val.sref.ref.rwLast = 205;
   xRef.val.sref.ref.colFirst = 1;
   xRef.val.sref.ref.colLast = 1;
   xValue.xltype = xltypeInt;
   xValue.val.w = iVal;
   Excel12(xlSet, 0, 2, (LPXLOPER12)&xRef, (LPXLOPER12)&xValue);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="94d21-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="94d21-134">See also</span></span>

- [<span data-ttu-id="94d21-135">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="94d21-135">xlCoerce</span></span>](xlcoerce.md)
- [<span data-ttu-id="94d21-136">Fonctions de l’API C à appeler à partir d’un fichier DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="94d21-136">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

