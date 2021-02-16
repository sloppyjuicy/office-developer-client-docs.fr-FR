---
title: xlfCaller
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfCaller
keywords:
- fonction xlfcaller [excel 2007]
localization_priority: Normal
ms.assetid: de4b119c-ae2e-4207-9783-8d5692a4d052
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fb788375504cefab75fde9513147c1d54acdaa07
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405729"
---
# <a name="xlfcaller"></a><span data-ttu-id="cb080-104">xlfCaller</span><span class="sxs-lookup"><span data-stu-id="cb080-104">xlfCaller</span></span>

 <span data-ttu-id="cb080-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="cb080-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="cb080-106">Retourne des informations sur la cellule, la plage de cellules, la commande d’un menu, l’outil d’une barre d’outils ou l’objet qui a appelé la commande ou la fonction DLL en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="cb080-106">Returns information about the cell, range of cells, command on a menu, tool on a toolbar, or object that called the DLL command or function that is currently running.</span></span>
  
|<span data-ttu-id="cb080-107">**Code appelé à partir de**</span><span class="sxs-lookup"><span data-stu-id="cb080-107">**Code called from**</span></span>|<span data-ttu-id="cb080-108">**Renvoie**</span><span class="sxs-lookup"><span data-stu-id="cb080-108">**Returns**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cb080-109">DLL</span><span class="sxs-lookup"><span data-stu-id="cb080-109">DLL</span></span>  <br/> |<span data-ttu-id="cb080-110">ID d’inscription.</span><span class="sxs-lookup"><span data-stu-id="cb080-110">The Register ID.</span></span>  <br/> |
|<span data-ttu-id="cb080-111">Une seule cellule</span><span class="sxs-lookup"><span data-stu-id="cb080-111">A single cell</span></span>  <br/> |<span data-ttu-id="cb080-112">Référence à une seule cellule.</span><span class="sxs-lookup"><span data-stu-id="cb080-112">A single-cell reference.</span></span>  <br/> |
|<span data-ttu-id="cb080-113">Formule de tableau à cellules multiples</span><span class="sxs-lookup"><span data-stu-id="cb080-113">A multi-cell array formula</span></span>  <br/> |<span data-ttu-id="cb080-114">Référence à plusieurs cellules.</span><span class="sxs-lookup"><span data-stu-id="cb080-114">A multi-cell reference.</span></span>  <br/> |
|<span data-ttu-id="cb080-115">Expression de mise en forme conditionnelle</span><span class="sxs-lookup"><span data-stu-id="cb080-115">A conditional formatting expression</span></span>  <br/> |<span data-ttu-id="cb080-116">Référence à la cellule à laquelle la condition de mise en forme est appliquée.</span><span class="sxs-lookup"><span data-stu-id="cb080-116">A reference to the cell to which the formatting condition is applied.</span></span>  <br/> |
|<span data-ttu-id="cb080-117">Un menu</span><span class="sxs-lookup"><span data-stu-id="cb080-117">A menu</span></span>  <br/> | <span data-ttu-id="cb080-118">Tableau à une seule ligne à quatre éléments :</span><span class="sxs-lookup"><span data-stu-id="cb080-118">A four-element single-row array:</span></span>  <br/>  <span data-ttu-id="cb080-119">ID de la barre.</span><span class="sxs-lookup"><span data-stu-id="cb080-119">The bar ID.</span></span>  <br/>  <span data-ttu-id="cb080-120">Position du menu.</span><span class="sxs-lookup"><span data-stu-id="cb080-120">The menu position.</span></span>  <br/>  <span data-ttu-id="cb080-121">Position du sous-menu.</span><span class="sxs-lookup"><span data-stu-id="cb080-121">The submenu position.</span></span>  <br/>  <span data-ttu-id="cb080-122">Position de la commande.</span><span class="sxs-lookup"><span data-stu-id="cb080-122">The command position.</span></span>  <br/> |
|<span data-ttu-id="cb080-123">Barre d’outils</span><span class="sxs-lookup"><span data-stu-id="cb080-123">A toolbar</span></span>  <br/> | <span data-ttu-id="cb080-124">Tableau à une seule ligne à deux éléments :</span><span class="sxs-lookup"><span data-stu-id="cb080-124">A two-element single-row array:</span></span>  <br/>  <span data-ttu-id="cb080-125">Numéro de barre d’outils pour les barres d’outils intégrées ou nom de barre d’outils pour les barres d’outils personnalisées.</span><span class="sxs-lookup"><span data-stu-id="cb080-125">The toolbar number for built-in toolbars or the toolbar name for custom toolbars.</span></span>  <br/>  <span data-ttu-id="cb080-126">Position sur la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="cb080-126">The position on the toolbar.</span></span>  <br/> |
|<span data-ttu-id="cb080-127">Objet graphique</span><span class="sxs-lookup"><span data-stu-id="cb080-127">A graphic object</span></span>  <br/> |<span data-ttu-id="cb080-128">Identificateur d’objet (nom de l’objet).</span><span class="sxs-lookup"><span data-stu-id="cb080-128">The object identifier (object name).</span></span>  <br/> |
|<span data-ttu-id="cb080-129">Commande associée à un xlcOnEnter, ON. ENTRÉE, capture d’événement</span><span class="sxs-lookup"><span data-stu-id="cb080-129">A command associated with an xlcOnEnter, ON.ENTER, event trap</span></span>  <br/> |<span data-ttu-id="cb080-130">Référence à la ou aux cellules entrées.</span><span class="sxs-lookup"><span data-stu-id="cb080-130">A reference to the cell or cells being entered.</span></span>  <br/> |
|<span data-ttu-id="cb080-131">Commande associée à un xlcOnDoubleclick, ON. DOUBLECLICK, capture d’événement.</span><span class="sxs-lookup"><span data-stu-id="cb080-131">A command associated with an xlcOnDoubleclick, ON.DOUBLECLICK, event trap.</span></span>  <br/> |<span data-ttu-id="cb080-132">Cellule sur qui l’utilisateur a double-cliqué (pas nécessairement la cellule active).</span><span class="sxs-lookup"><span data-stu-id="cb080-132">The cell that was double-clicked (not necessarily the active cell).</span></span>  <br/> |
|<span data-ttu-id="cb080-133">Auto_Open, AutoClose, Auto_Activate ou Auto_Deactivate macro</span><span class="sxs-lookup"><span data-stu-id="cb080-133">Auto_Open, AutoClose, Auto_Activate or Auto_Deactivate macro</span></span>  <br/> |<span data-ttu-id="cb080-134">Nom de la feuille d’appel.</span><span class="sxs-lookup"><span data-stu-id="cb080-134">The name of the calling sheet.</span></span>  <br/> |
|<span data-ttu-id="cb080-135">Autres méthodes non répertoriées</span><span class="sxs-lookup"><span data-stu-id="cb080-135">Other methods not listed</span></span>  <br/> |<span data-ttu-id="cb080-136">#REF!</span><span class="sxs-lookup"><span data-stu-id="cb080-136">#REF!</span></span> <span data-ttu-id="cb080-137">Erreur</span><span class="sxs-lookup"><span data-stu-id="cb080-137">Error.</span></span>  <br/> |
   
```cs
Excel12(xlfCaller, (LPXLOPER12) pxRes,0);
```

## <a name="property-valuereturn-value"></a><span data-ttu-id="cb080-138">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="cb080-138">Property value/Return value</span></span>

<span data-ttu-id="cb080-139">La valeur de retour est l’un des types de données **XLOPER** /  **XLOPER12** suivants : **xltypeRef**, **xltypeSRef**, **xltypeNum**, **xltypeStr**, **xltypeErr** ou **xltypeMulti**.</span><span class="sxs-lookup"><span data-stu-id="cb080-139">The return value is one of the following **XLOPER**/ **XLOPER12** data types: **xltypeRef**, **xltypeSRef**, **xltypeNum**, **xltypeStr**, **xltypeErr**, or **xltypeMulti**.</span></span> <span data-ttu-id="cb080-140">Étant donné que trois de ces types pointent vers la mémoire allouée, la valeur de retour de **xlfCaller** doit toujours être libérée dans un appel à la fonction [xlFree](xlfree.md) lorsqu’elle n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="cb080-140">Since three of these types point to allocated memory, the return value of **xlfCaller** should always be freed in a call to the [xlFree function](xlfree.md) when it is no longer needed.</span></span> 
  
<span data-ttu-id="cb080-141">Pour plus d’informations **sur xlOPERs** /  **XLOPER12,** voir [Gestion de la mémoire dans Excel.](memory-management-in-excel.md)</span><span class="sxs-lookup"><span data-stu-id="cb080-141">For more information about **XLOPERs**/ **XLOPER12s** see [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cb080-142">Remarques</span><span class="sxs-lookup"><span data-stu-id="cb080-142">Remarks</span></span>

<span data-ttu-id="cb080-143">Cette fonction est la seule fonction non-feuille de calcul qui peut être appelée à partir d’une fonction de feuille de calcul DLL/XLL.</span><span class="sxs-lookup"><span data-stu-id="cb080-143">This function is the only non-worksheet function that can be called from a DLL/XLL worksheet function.</span></span> <span data-ttu-id="cb080-144">D’autres fonctions d’informations XLM peuvent uniquement être appelées à partir de commandes ou de fonctions équivalentes à une feuille macro.</span><span class="sxs-lookup"><span data-stu-id="cb080-144">Other XLM information functions can only be called from commands or macro-sheet equivalent functions.</span></span>
  
## <a name="example"></a><span data-ttu-id="cb080-145">Exemple</span><span class="sxs-lookup"><span data-stu-id="cb080-145">Example</span></span>

 <span data-ttu-id="cb080-146">`\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="cb080-146">`\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span> <span data-ttu-id="cb080-147">Cette fonction appelle une macro de commande (xlcSelect) et ne fonctionne correctement qu’en cas d’appel à partir d’une feuille macro.</span><span class="sxs-lookup"><span data-stu-id="cb080-147">This function calls a command macro (xlcSelect) and will work correctly only when called from a macro sheet.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="cb080-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb080-148">See also</span></span>



[<span data-ttu-id="cb080-149">Fonctions XLM essentielles et utiles de l’API C</span><span class="sxs-lookup"><span data-stu-id="cb080-149">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

