---
title: xlfCaller
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfCaller
keywords:
- fonction xlfCaller [Excel 2007]
localization_priority: Normal
ms.assetid: de4b119c-ae2e-4207-9783-8d5692a4d052
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: fb788375504cefab75fde9513147c1d54acdaa07
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310226"
---
# <a name="xlfcaller"></a><span data-ttu-id="e3ed6-104">xlfCaller</span><span class="sxs-lookup"><span data-stu-id="e3ed6-104">xlfCaller</span></span>

 <span data-ttu-id="e3ed6-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e3ed6-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="e3ed6-106">Renvoie des informations sur la cellule, une plage de cellules, une commande d'un menu, un outil sur une barre d'outils ou un objet qui a appelé la commande ou la fonction DLL en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="e3ed6-106">Returns information about the cell, range of cells, command on a menu, tool on a toolbar, or object that called the DLL command or function that is currently running.</span></span>
  
|<span data-ttu-id="e3ed6-107">**Code appelé depuis**</span><span class="sxs-lookup"><span data-stu-id="e3ed6-107">**Code called from**</span></span>|<span data-ttu-id="e3ed6-108">**Renvoie**</span><span class="sxs-lookup"><span data-stu-id="e3ed6-108">**Returns**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e3ed6-109">FICHIER</span><span class="sxs-lookup"><span data-stu-id="e3ed6-109">DLL</span></span>  <br/> |<span data-ttu-id="e3ed6-110">ID de registre.</span><span class="sxs-lookup"><span data-stu-id="e3ed6-110">The Register ID.</span></span>  <br/> |
|<span data-ttu-id="e3ed6-111">Une cellule unique</span><span class="sxs-lookup"><span data-stu-id="e3ed6-111">A single cell</span></span>  <br/> |<span data-ttu-id="e3ed6-112">Une référence à cellule unique.</span><span class="sxs-lookup"><span data-stu-id="e3ed6-112">A single-cell reference.</span></span>  <br/> |
|<span data-ttu-id="e3ed6-113">Une formule matricielle à cellules multiples</span><span class="sxs-lookup"><span data-stu-id="e3ed6-113">A multi-cell array formula</span></span>  <br/> |<span data-ttu-id="e3ed6-114">Une référence à plusieurs cellules.</span><span class="sxs-lookup"><span data-stu-id="e3ed6-114">A multi-cell reference.</span></span>  <br/> |
|<span data-ttu-id="e3ed6-115">Expression de mise en forme conditionnelle</span><span class="sxs-lookup"><span data-stu-id="e3ed6-115">A conditional formatting expression</span></span>  <br/> |<span data-ttu-id="e3ed6-116">Référence à la cellule à laquelle la condition de mise en forme est appliquée.</span><span class="sxs-lookup"><span data-stu-id="e3ed6-116">A reference to the cell to which the formatting condition is applied.</span></span>  <br/> |
|<span data-ttu-id="e3ed6-117">Un menu</span><span class="sxs-lookup"><span data-stu-id="e3ed6-117">A menu</span></span>  <br/> | <span data-ttu-id="e3ed6-118">Un tableau à ligne unique à quatre éléments:</span><span class="sxs-lookup"><span data-stu-id="e3ed6-118">A four-element single-row array:</span></span>  <br/>  <span data-ttu-id="e3ed6-119">ID de la barre.</span><span class="sxs-lookup"><span data-stu-id="e3ed6-119">The bar ID.</span></span>  <br/>  <span data-ttu-id="e3ed6-120">Position du menu.</span><span class="sxs-lookup"><span data-stu-id="e3ed6-120">The menu position.</span></span>  <br/>  <span data-ttu-id="e3ed6-121">Position du sous-menu.</span><span class="sxs-lookup"><span data-stu-id="e3ed6-121">The submenu position.</span></span>  <br/>  <span data-ttu-id="e3ed6-122">Position de la commande.</span><span class="sxs-lookup"><span data-stu-id="e3ed6-122">The command position.</span></span>  <br/> |
|<span data-ttu-id="e3ed6-123">Barre d'outils</span><span class="sxs-lookup"><span data-stu-id="e3ed6-123">A toolbar</span></span>  <br/> | <span data-ttu-id="e3ed6-124">Un tableau à une seule ligne à deux éléments:</span><span class="sxs-lookup"><span data-stu-id="e3ed6-124">A two-element single-row array:</span></span>  <br/>  <span data-ttu-id="e3ed6-125">Numéro de la barre d'outils pour les barres d'outils intégrées ou nom de la barre d'outils pour les barres d'outils personnalisées.</span><span class="sxs-lookup"><span data-stu-id="e3ed6-125">The toolbar number for built-in toolbars or the toolbar name for custom toolbars.</span></span>  <br/>  <span data-ttu-id="e3ed6-126">Position de la barre d'outils.</span><span class="sxs-lookup"><span data-stu-id="e3ed6-126">The position on the toolbar.</span></span>  <br/> |
|<span data-ttu-id="e3ed6-127">Un objet graphique</span><span class="sxs-lookup"><span data-stu-id="e3ed6-127">A graphic object</span></span>  <br/> |<span data-ttu-id="e3ed6-128">Identificateur d'objet (nom de l'objet).</span><span class="sxs-lookup"><span data-stu-id="e3ed6-128">The object identifier (object name).</span></span>  <br/> |
|<span data-ttu-id="e3ed6-129">Commande associée à un xlcOnEnter, ON. ENTRÉE, notification d'événement</span><span class="sxs-lookup"><span data-stu-id="e3ed6-129">A command associated with an xlcOnEnter, ON.ENTER, event trap</span></span>  <br/> |<span data-ttu-id="e3ed6-130">Référence à la ou aux cellules entrées.</span><span class="sxs-lookup"><span data-stu-id="e3ed6-130">A reference to the cell or cells being entered.</span></span>  <br/> |
|<span data-ttu-id="e3ed6-131">Commande associée à un xlcOnDoubleclick, ON. DOUBLECLICK, reception d'événement.</span><span class="sxs-lookup"><span data-stu-id="e3ed6-131">A command associated with an xlcOnDoubleclick, ON.DOUBLECLICK, event trap.</span></span>  <br/> |<span data-ttu-id="e3ed6-132">Cellule sur laquelle l'utilisateur a cliqué deux fois (pas nécessairement la cellule active).</span><span class="sxs-lookup"><span data-stu-id="e3ed6-132">The cell that was double-clicked (not necessarily the active cell).</span></span>  <br/> |
|<span data-ttu-id="e3ed6-133">Auto_Open, AutoClose, Auto_Activate ou Auto_Deactivate, macro</span><span class="sxs-lookup"><span data-stu-id="e3ed6-133">Auto_Open, AutoClose, Auto_Activate or Auto_Deactivate macro</span></span>  <br/> |<span data-ttu-id="e3ed6-134">Nom de la feuille d'appel.</span><span class="sxs-lookup"><span data-stu-id="e3ed6-134">The name of the calling sheet.</span></span>  <br/> |
|<span data-ttu-id="e3ed6-135">Autres méthodes non indiquées</span><span class="sxs-lookup"><span data-stu-id="e3ed6-135">Other methods not listed</span></span>  <br/> |<span data-ttu-id="e3ed6-136">#REF!</span><span class="sxs-lookup"><span data-stu-id="e3ed6-136">#REF!</span></span> <span data-ttu-id="e3ed6-137">Erreur</span><span class="sxs-lookup"><span data-stu-id="e3ed6-137">Error.</span></span>  <br/> |
   
```cs
Excel12(xlfCaller, (LPXLOPER12) pxRes,0);
```

## <a name="property-valuereturn-value"></a><span data-ttu-id="e3ed6-138">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="e3ed6-138">Property value/Return value</span></span>

<span data-ttu-id="e3ed6-139">La valeur renvoyée est l'un des types de données**XLOPER12** d' **XLOPER**/ suivants: **xltypeRef**, **xltypeSRef**, **xltypeNum**, **xltypeStr**, **xltypeErr**ou **xltypeMulti**.</span><span class="sxs-lookup"><span data-stu-id="e3ed6-139">The return value is one of the following **XLOPER**/ **XLOPER12** data types: **xltypeRef**, **xltypeSRef**, **xltypeNum**, **xltypeStr**, **xltypeErr**, or **xltypeMulti**.</span></span> <span data-ttu-id="e3ed6-140">Étant donné que trois de ces types pointent vers la mémoire allouée, la valeur de retour de **xlfCaller** doit toujours être libérée dans un appel à la [fonction xlFree](xlfree.md) lorsqu'elle n'est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="e3ed6-140">Since three of these types point to allocated memory, the return value of **xlfCaller** should always be freed in a call to the [xlFree function](xlfree.md) when it is no longer needed.</span></span> 
  
<span data-ttu-id="e3ed6-141">Pour plus d'informations sur les **XLOPER**/ **XLOPER12** , consultez la rubrique [gestion de la mémoire dans Excel](memory-management-in-excel.md).</span><span class="sxs-lookup"><span data-stu-id="e3ed6-141">For more information about **XLOPERs**/ **XLOPER12s** see [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e3ed6-142">Remarques</span><span class="sxs-lookup"><span data-stu-id="e3ed6-142">Remarks</span></span>

<span data-ttu-id="e3ed6-143">Cette fonction n'est pas une fonction de feuille de calcul qui peut être appelée à partir d'une fonction de feuille de calcul DLL/XLL.</span><span class="sxs-lookup"><span data-stu-id="e3ed6-143">This function is the only non-worksheet function that can be called from a DLL/XLL worksheet function.</span></span> <span data-ttu-id="e3ed6-144">Les autres fonctions d'informations XLM ne peuvent être appelées qu'à partir de commandes ou de fonctions équivalentes de feuille macro.</span><span class="sxs-lookup"><span data-stu-id="e3ed6-144">Other XLM information functions can only be called from commands or macro-sheet equivalent functions.</span></span>
  
## <a name="example"></a><span data-ttu-id="e3ed6-145">Exemple</span><span class="sxs-lookup"><span data-stu-id="e3ed6-145">Example</span></span>

 <span data-ttu-id="e3ed6-146">`\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="e3ed6-146"></span></span> <span data-ttu-id="e3ed6-147">Cette fonction appelle une macro de commande (xlcSelect) et fonctionne correctement uniquement lorsqu'elle est appelée à partir d'une feuille macro.</span><span class="sxs-lookup"><span data-stu-id="e3ed6-147">This function calls a command macro (xlcSelect) and will work correctly only when called from a macro sheet.</span></span>
  
```cs
short WINAPI CallerExample(void)
{
   XLOPER12 xRes;
   Excel12(xlfCaller, &xRes, 0);
   Excel12(xlcSelect, 0, 1, (LPXLOPER12)&xRes);
   Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="e3ed6-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3ed6-148">See also</span></span>



[<span data-ttu-id="e3ed6-149">Fonctions XLM essentielles et utiles de l’API C</span><span class="sxs-lookup"><span data-stu-id="e3ed6-149">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

