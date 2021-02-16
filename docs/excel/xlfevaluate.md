---
title: xlfEvaluate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfEvaluate
keywords:
- fonction xlfevaluate [excel 2007]
localization_priority: Normal
ms.assetid: deea3ee6-2a32-47ef-bfa4-914891538633
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 527f7e932a41103c374e327a1bd0dd4c7d8e92a0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439183"
---
# <a name="xlfevaluate"></a><span data-ttu-id="da4e1-104">xlfEvaluate</span><span class="sxs-lookup"><span data-stu-id="da4e1-104">xlfEvaluate</span></span>

 <span data-ttu-id="da4e1-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="da4e1-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="da4e1-106">Utilise l’analyseur et l’évaluateur de fonction Microsoft Excel pour évaluer toute expression qui pourrait être entrée dans une cellule de feuille de calcul.</span><span class="sxs-lookup"><span data-stu-id="da4e1-106">Uses the Microsoft Excel parser and function evaluator to evaluate any expression that could be entered in a worksheet cell.</span></span>
  
```cs
Excel12(xlfEvaluate, LPXLOPER12 pxRes, 1, LPXLOPER12 pxFormulaText);
```

## <a name="parameters"></a><span data-ttu-id="da4e1-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="da4e1-107">Parameters</span></span>

 <span data-ttu-id="da4e1-108">_pxFormulaText (xltypeStr)_</span><span class="sxs-lookup"><span data-stu-id="da4e1-108">_pxFormulaText (xltypeStr)_</span></span>
  
<span data-ttu-id="da4e1-109">Chaîne à évaluer.</span><span class="sxs-lookup"><span data-stu-id="da4e1-109">The string to be evaluated.</span></span> <span data-ttu-id="da4e1-110">Un signe égal de premier plan (=) est facultatif.</span><span class="sxs-lookup"><span data-stu-id="da4e1-110">A leading equal sign (=) is optional.</span></span> <span data-ttu-id="da4e1-111">La chaîne peut être n’importe quel texte qui peut légalement être entré dans une feuille de calcul ou une cellule de feuille de macro.</span><span class="sxs-lookup"><span data-stu-id="da4e1-111">The string can be any text that can legally be entered into a worksheet or macro sheet cell.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="da4e1-112">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="da4e1-112">Property value/Return value</span></span>

<span data-ttu-id="da4e1-113">Renvoie le résultat de l’évaluation de la chaîne qui peut être l’un des types **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeNil**, **xltypeMulti**.</span><span class="sxs-lookup"><span data-stu-id="da4e1-113">Returns the result of evaluating the string which can be any of the types **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeNil**, **xltypeMulti**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="da4e1-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="da4e1-114">Remarks</span></span>

<span data-ttu-id="da4e1-115">La chaîne peut contenir uniquement des fonctions, et non des équivalents de commande.</span><span class="sxs-lookup"><span data-stu-id="da4e1-115">The string can contain only functions, not command equivalents.</span></span> <span data-ttu-id="da4e1-116">Cela équivaut à appuyer sur **F9 à** partir de la barre de formule.</span><span class="sxs-lookup"><span data-stu-id="da4e1-116">It is equivalent to pressing **F9** from the formula bar.</span></span> <span data-ttu-id="da4e1-117">Si **xlfEvaluate** est appelé à partir d’une fonction de feuille de calcul XLL inscrite comme thread-safe, l’expression ne doit contenir que des fonctions thread-safe.</span><span class="sxs-lookup"><span data-stu-id="da4e1-117">If **xlfEvaluate** is called from an XLL worksheet function that has been registered as thread safe, the expression must only contain thread-safe functions.</span></span> 
  
<span data-ttu-id="da4e1-118">L’utilisation principale de la fonction **xlfEvaluate** consiste à autoriser les DLL à rechercher la valeur affectée à un nom défini qui se trouve sur une feuille ou un nom masqué défini dans la DLL.</span><span class="sxs-lookup"><span data-stu-id="da4e1-118">The primary use of the **xlfEvaluate** function is to allow DLLs to find out the value assigned to a defined name that is either on a sheet or a hidden name defined within the DLL.</span></span> <span data-ttu-id="da4e1-119">Notez qu’au sein d’une DLL/XLL, un nom de feuille de calcul doit être précédé d’au moins un point d’exclamation (!) pour garantir qu’il est interprété comme externe à la DLL.</span><span class="sxs-lookup"><span data-stu-id="da4e1-119">Note that within a DLL/XLL, a worksheet name must be prefixed with at least an exclamation mark (!) to ensure that it is interpreted as external to the DLL.</span></span> <span data-ttu-id="da4e1-120">Pour plus d’informations, voir [l’évaluation des noms et d’autres expressions de](evaluating-names-and-other-worksheet-formula-expressions.md)formule de feuille de calcul.</span><span class="sxs-lookup"><span data-stu-id="da4e1-120">For more information, see [Evaluating Names and Other Worksheet Formula Expressions](evaluating-names-and-other-worksheet-formula-expressions.md).</span></span>
  
 <span data-ttu-id="da4e1-121">**xlfEvaluate ne peut** pas être utilisé pour évaluer les références à une feuille externe qui n’est pas ouverte.</span><span class="sxs-lookup"><span data-stu-id="da4e1-121">**xlfEvaluate** cannot be used to evaluate references to an external sheet that is not open.</span></span> 
  
## <a name="example"></a><span data-ttu-id="da4e1-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="da4e1-122">Example</span></span>

<span data-ttu-id="da4e1-123">Cet exemple utilise **xlfEvaluate** pour forcer le texte « ! B38 " au contenu de la cellule B38.</span><span class="sxs-lookup"><span data-stu-id="da4e1-123">This example uses **xlfEvaluate** to coerce the text "!B38" to the contents of cell B38.</span></span> 
  
 <span data-ttu-id="da4e1-124">`\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="da4e1-124">`\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span> <span data-ttu-id="da4e1-125">Cette fonction appelle une macro de commande (**xlcAlert**) et ne fonctionne correctement qu’en cas d’appel à partir d’une feuille macro ou d’une commande macro.</span><span class="sxs-lookup"><span data-stu-id="da4e1-125">This function calls a command macro (**xlcAlert**) and will work correctly only when called from a macro sheet or as a macro command.</span></span>
  
```cs
short WINAPI EvaluateExample(void)
{
    XLOPER12 xFormulaText, xRes, xRes2, xInt;
    xFormulaText.xltype = xltypeStr;
    xFormulaText.val.str = L"\004!B38";
    Excel12(xlfEvaluate, &xRes, 1, (LPXLOPER12)&xFormulaText);
    xInt.xltype = xltypeInt;
    xInt.val.w = 2;
    Excel12(xlcAlert, &xRes2, 2, (LPXLOPER12)&xRes, (LPXLOPER12)&xInt);
    Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
    Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes2);
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="da4e1-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da4e1-126">See also</span></span>

- [<span data-ttu-id="da4e1-127">Fonctions XLM essentielles et utiles de l’API C</span><span class="sxs-lookup"><span data-stu-id="da4e1-127">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

