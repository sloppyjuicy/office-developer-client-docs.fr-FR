---
title: xlSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSet
keywords:
- fonction xlSet [excel 2007]
localization_priority: Normal
ms.assetid: 121e6212-0692-4430-97be-4792b53719bf
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 63f50e441f5d851677f36754a17bcd6403705239
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782247"
---
# <a name="xlset"></a><span data-ttu-id="2a10f-104">xlSet</span><span class="sxs-lookup"><span data-stu-id="2a10f-104">xlSet</span></span>

<span data-ttu-id="2a10f-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2a10f-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="2a10f-106">Place les valeurs de constantes dans des cellules ou plages très rapidement.</span><span class="sxs-lookup"><span data-stu-id="2a10f-106">Puts constant values into cells or ranges very quickly.</span></span> <span data-ttu-id="2a10f-107">Pour plus d’informations, voir « xlSet et classeurs avec des formules matricielles » dans [Les problèmes connus dans le développement de XLL Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="2a10f-107">For more information, see "xlSet and Workbooks with Array Formulas" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel12(xlSet, LPXLOPER12 pxRes, 2, LPXLOPER12 pxReference, LPXLOPER pxValue);
```

## <a name="parameters"></a><span data-ttu-id="2a10f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2a10f-108">Parameters</span></span>

<span data-ttu-id="2a10f-109">_pxReference_ (**xltypeRef** ou **xltypeSRef**)</span><span class="sxs-lookup"><span data-stu-id="2a10f-109">_pxReference_ (**xltypeRef** or **xltypeSRef**)</span></span>
  
<span data-ttu-id="2a10f-110">Référence rectangulaire décrivant la cible ou les cellules.</span><span class="sxs-lookup"><span data-stu-id="2a10f-110">A rectangular reference describing the target cell or cells.</span></span> <span data-ttu-id="2a10f-111">La référence doit décrire les cellules adjacentes, ainsi que dans une **xltypeRef** `val.mref.lpmref->count` doit être défini sur 1.</span><span class="sxs-lookup"><span data-stu-id="2a10f-111">The reference must describe adjacent cells, so that in an **xltypeRef** `val.mref.lpmref->count` must be set to 1.</span></span> 
  
<span data-ttu-id="2a10f-112">_pxValue_</span><span class="sxs-lookup"><span data-stu-id="2a10f-112">_pxValue_</span></span>
  
<span data-ttu-id="2a10f-113">L’ou les valeurs à placer dans l’ou les cellules.</span><span class="sxs-lookup"><span data-stu-id="2a10f-113">The value or values to be placed into the cell or cells.</span></span> <span data-ttu-id="2a10f-114">Pour plus d’informations, voir la section « Remarques ».</span><span class="sxs-lookup"><span data-stu-id="2a10f-114">For more information, see the "Remarks" section.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2a10f-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="2a10f-115">Remarks</span></span>

### <a name="pxvalue-argument"></a><span data-ttu-id="2a10f-116">argument pxValue</span><span class="sxs-lookup"><span data-stu-id="2a10f-116">pxValue argument</span></span>

<span data-ttu-id="2a10f-117">_pxValue_ peut être une valeur ou un tableau.</span><span class="sxs-lookup"><span data-stu-id="2a10f-117">_pxValue_ can either be a value or an array.</span></span> <span data-ttu-id="2a10f-118">Si elle est une valeur, la plage de destination entière est remplie avec cette valeur.</span><span class="sxs-lookup"><span data-stu-id="2a10f-118">If it is a value, the entire destination range is filled with that value.</span></span> <span data-ttu-id="2a10f-119">S’il est un tableau (**xltypeMulti**), les éléments du tableau sont placés dans les emplacements correspondants dans le rectangle.</span><span class="sxs-lookup"><span data-stu-id="2a10f-119">If it is an array (**xltypeMulti**), the elements of the array are put into the corresponding locations in the rectangle.</span></span>
  
<span data-ttu-id="2a10f-120">Si vous utilisez une matrice pour le second argument, elle est dupliquée vers le bas pour remplir l’ensemble du rectangle.</span><span class="sxs-lookup"><span data-stu-id="2a10f-120">If you use a horizontal array for the second argument, it is duplicated down to fill the entire rectangle.</span></span> <span data-ttu-id="2a10f-121">Si vous utilisez une matrice verticale, elle est dupliquée de droite à remplir l’ensemble du rectangle.</span><span class="sxs-lookup"><span data-stu-id="2a10f-121">If you use a vertical array, it is duplicated right to fill the entire rectangle.</span></span> <span data-ttu-id="2a10f-122">Si vous utilisez un tableau rectangulaire, et il est trop petit pour la plage rectangulaire dans que doivent figurer, cette plage est remplie avec s **# N/a**.</span><span class="sxs-lookup"><span data-stu-id="2a10f-122">If you use a rectangular array, and it is too small for the rectangular range you want to put it in, that range is padded with **#N/A**s.</span></span>
  
<span data-ttu-id="2a10f-123">Si la plage cible est inférieure à la baie source, les valeurs sont copiées dans les limites de la plage cible et les données supplémentaires sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="2a10f-123">If the target range is smaller than the source array, the values are copied in up to the limits of the target range and the extra data are ignored.</span></span>
  
<span data-ttu-id="2a10f-124">Pour supprimer un élément du rectangle de destination, utilisez un élément de tableau de type **xltypeNil** dans le tableau source.</span><span class="sxs-lookup"><span data-stu-id="2a10f-124">To clear an element of the destination rectangle, use an **xltypeNil** type array element in the source array.</span></span> <span data-ttu-id="2a10f-125">Pour effacer le rectangle de destination entière, omettez le deuxième argument.</span><span class="sxs-lookup"><span data-stu-id="2a10f-125">To clear the entire destination rectangle, omit the second argument.</span></span> 
  
### <a name="restrictions"></a><span data-ttu-id="2a10f-126">Restrictions</span><span class="sxs-lookup"><span data-stu-id="2a10f-126">Restrictions</span></span>

<span data-ttu-id="2a10f-127">**xlSet** ne peut pas être annulée.</span><span class="sxs-lookup"><span data-stu-id="2a10f-127">**xlSet** cannot be undone.</span></span> <span data-ttu-id="2a10f-128">En outre, il supprime toutes les informations annulation sont peut-être disponibles avant.</span><span class="sxs-lookup"><span data-stu-id="2a10f-128">In addition, it destroys any undo information that may have been available before.</span></span> 
  
<span data-ttu-id="2a10f-129">**xlSet** pouvez placer uniquement des constantes, ni les formules dans des cellules.</span><span class="sxs-lookup"><span data-stu-id="2a10f-129">**xlSet** can put only constants, not formulas, into cells.</span></span> 
  
<span data-ttu-id="2a10f-130">**xlSet** se comporte comme une fonction équivaut à la commande de classe 3 ; Autrement dit, il est disponible uniquement à l’intérieur d’une DLL lorsque la DLL est appelée à partir d’un objet, macro, menu, barre d’outils, touche de raccourci ou le bouton **exécuter** dans la boîte de dialogue **Macro** (accédé à partir de l’onglet **affichage** du ruban à compter d’Excel 2007 et les outils ** **menu dans les versions antérieures).</span><span class="sxs-lookup"><span data-stu-id="2a10f-130">**xlSet** behaves as a Class 3 command-equivalent function; that is, it is available only inside a DLL when the DLL is called from an object, macro, menu, toolbar, shortcut key, or the **Run** button in the **Macro** dialog box (accessed from **View** tab on the ribbon starting in Excel 2007, and the **Tools** menu in earlier versions).</span></span> 
  
## <a name="example"></a><span data-ttu-id="2a10f-131">Exemple</span><span class="sxs-lookup"><span data-stu-id="2a10f-131">Example</span></span>

<span data-ttu-id="2a10f-132">L’exemple suivant remplit B205:B206 avec la valeur qui a été passée à partir d’une macro.</span><span class="sxs-lookup"><span data-stu-id="2a10f-132">The following example fills B205:B206 with the value that was passed in from a macro.</span></span> <span data-ttu-id="2a10f-133">Cet exemple de fonction commande requiert un argument et donc ne fonctionnera que si elle est appelée à partir d’une feuille de macro XLM, ou d’un module VBA à l’aide de la méthode **Application.Run** .</span><span class="sxs-lookup"><span data-stu-id="2a10f-133">This command function example requires an argument, and so will only work if called from an XLM macro sheet, or from a VBA module using the **Application.Run** method.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="2a10f-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2a10f-134">See also</span></span>

- [<span data-ttu-id="2a10f-135">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="2a10f-135">xlCoerce</span></span>](xlcoerce.md)
- [<span data-ttu-id="2a10f-136">Fonctions de l’API C qui peuvent être appelées uniquement à partir d’une DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="2a10f-136">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

