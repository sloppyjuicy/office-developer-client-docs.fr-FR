---
title: Évaluation des noms et d’autres expressions de formule dans les feuilles de calcul
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- expression evaluation [excel 2007],worksheets [Excel 2007], name evaluation,evaluating expressions [Excel 2007],evaluating worksheet names [Excel 2007],expressions [Excel 2007], evaluating,names [Excel 2007],expressions [Excel 2007], evaluating,names [Excel 2007] Excel 2007], evaluating,name evaluation [Excel 2007],strings [Excel 2007], converting to values,xlfEvaluate function [Excel 2007],worksheets [Excel 2007], expression evaluation
localization_priority: Normal
ms.assetid: 2b23c75e-2a95-4f26-8714-2a73f5e326a7
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 97328cbc57a9144a133524774e3be10a84a96bf4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406863"
---
# <a name="evaluating-names-and-other-worksheet-formula-expressions"></a><span data-ttu-id="7803e-104">Évaluation des noms et d’autres expressions de formule dans les feuilles de calcul</span><span class="sxs-lookup"><span data-stu-id="7803e-104">Evaluating names and other worksheet formula expressions</span></span>

<span data-ttu-id="7803e-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7803e-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="7803e-106">L’une des fonctionnalités les plus importantes exposées par Excel via l’API C est la possibilité de convertir toute formule de chaîne qui peut légalement être entrée dans une feuille de calcul en une valeur ou un tableau de valeurs.</span><span class="sxs-lookup"><span data-stu-id="7803e-106">One of the most important features that Excel exposes through the C API is the ability to convert any string formula that can legally be entered into a worksheet to a value, or array of values.</span></span> <span data-ttu-id="7803e-107">Cela est essentiel pour les fonctions et commandes XLL qui doivent lire le contenu des noms définis, par exemple.</span><span class="sxs-lookup"><span data-stu-id="7803e-107">This is essential for XLL functions and commands that must read the contents of defined names, for example.</span></span> <span data-ttu-id="7803e-108">Cette capacité est exposée par le biais de la fonction [xlfEvaluate,](xlfevaluate.md)comme illustré dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="7803e-108">This ability is exposed through the [xlfEvaluate function](xlfevaluate.md), as shown in this example.</span></span>
  
```C
int WINAPI evaluate_name_example(void)
{
  wchar_t *expression = L"\016!MyDefinedName";
  XLOPER12 xNameText, xNameValue;
  xNameText.xltype = xltypeStr;
  xNameText.val.str = expression;
// Try to evaluate the name. Will fail with a #NAME? error
// if MyDefinedName is not defined in the active workbook.
  Excel12(xlfEvaluate, &xNameValue, 1, &xNameText);
// Attempt to convert the value to a string and display it in
// an alert dialog. This fails if xNameValue is an error value.
  Excel12(xlcAlert, 0, 1, &xNameValue);
// Must free xNameValue in case MyDefinedName evaluated to a string
  Excel12(xlFree, 0, 1, &xNameValue);
  return 1;
}
```

<span data-ttu-id="7803e-109">Notez que lorsque vous évaluez un nom de feuille de calcul, soit seul, soit dans une formule, vous devez au moins faire précéder le nom par « ! ».</span><span class="sxs-lookup"><span data-stu-id="7803e-109">Note that when you are evaluating a worksheet name, either on its own or in a formula, you must prefix the name with '!', at least.</span></span> <span data-ttu-id="7803e-110">Sinon, Excel tente de trouver le nom dans un espace de noms masqué réservé aux DLLs.</span><span class="sxs-lookup"><span data-stu-id="7803e-110">Otherwise, Excel tries to find the name in a hidden namespace reserved for DLLs.</span></span> <span data-ttu-id="7803e-111">Vous pouvez créer et supprimer des noms de DLL masqués à l’aide de la [fonction xlfSetName](xlfsetname.md).</span><span class="sxs-lookup"><span data-stu-id="7803e-111">You can create and delete hidden DLL names using the [xlfSetName function](xlfsetname.md).</span></span> <span data-ttu-id="7803e-112">Vous pouvez obtenir la définition de n’importe quel nom défini, qu’il s’agit d’un nom DLL masqué ou d’un nom de feuille de calcul, à l’aide de la fonction **xlfGetDef.**</span><span class="sxs-lookup"><span data-stu-id="7803e-112">You can get the definition of any defined name, whether it is a hidden DLL name or a worksheet name, using the **xlfGetDef** function.</span></span> 
  
<span data-ttu-id="7803e-113">La spécification complète d’un nom de feuille de calcul se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="7803e-113">The full specification for a worksheet name takes the following form:</span></span>
  
`='C:\example folder\[Book1.xls]Sheet1'!Name`
  
<span data-ttu-id="7803e-114">Notez que Excel 2007 a introduit un certain nombre de nouvelles extensions de fichier.</span><span class="sxs-lookup"><span data-stu-id="7803e-114">Note that Excel 2007 introduced a number of new file extensions.</span></span> <span data-ttu-id="7803e-115">Vous pouvez omettre le chemin d’accès, le nom du Excel feuille et le nom de la feuille sans ambiguïté.</span><span class="sxs-lookup"><span data-stu-id="7803e-115">You can omit the path, the workbook name, and the sheet name where there is no ambiguity among the open workbooks in this Excel session.</span></span> 
  
<span data-ttu-id="7803e-116">L’exemple suivant évalue la formule de la feuille de calcul active et  `COUNT(A1:IV65536)` affiche le résultat.</span><span class="sxs-lookup"><span data-stu-id="7803e-116">The next example evaluates the formula  `COUNT(A1:IV65536)` for the active worksheet and displays the result.</span></span> <span data-ttu-id="7803e-117">Notez la nécessité de préfixer l’adresse de la plage par « ! » qui est cohérente avec la convention de référence de plage sur les feuilles macro XLM.</span><span class="sxs-lookup"><span data-stu-id="7803e-117">Note the need to prefix the range address with '!', which is consistent with the range reference convention on XLM macro sheets.</span></span> <span data-ttu-id="7803e-118">La XME de l’API C suit cette convention :</span><span class="sxs-lookup"><span data-stu-id="7803e-118">The C API XLM follows this convention:</span></span> 
  
- <span data-ttu-id="7803e-119">`=A1` Référence à la cellule A1 de la feuille macro actuelle.</span><span class="sxs-lookup"><span data-stu-id="7803e-119">`=A1` A reference to cell A1 on the current macro sheet.</span></span> <span data-ttu-id="7803e-120">(Non défini pour les XL).</span><span class="sxs-lookup"><span data-stu-id="7803e-120">(Not defined for XLLs).</span></span> 
  
- <span data-ttu-id="7803e-121">`=!A1` Référence à la cellule A1 de la feuille active (qui peut être une feuille de calcul ou une feuille macro)</span><span class="sxs-lookup"><span data-stu-id="7803e-121">`=!A1` A reference to cell A1 on the active sheet (which could be a worksheet or macro sheet)</span></span> 
  
- <span data-ttu-id="7803e-122">`=Sheet1!A1` Référence à la cellule A1 de la feuille spécifiée, Sheet1 dans ce cas.</span><span class="sxs-lookup"><span data-stu-id="7803e-122">`=Sheet1!A1` A reference to cell A1 on the specified sheet, Sheet1 in this case.</span></span> 
  
- <span data-ttu-id="7803e-123">`=[Book1.xls]Sheet1!A1` Référence à la cellule A1 de la feuille spécifiée dans le livre de travail spécifié.</span><span class="sxs-lookup"><span data-stu-id="7803e-123">`=[Book1.xls]Sheet1!A1` A reference to cell A1 on the specified sheet in the specified workbook.</span></span> 
  
<span data-ttu-id="7803e-124">Dans une XLL, une référence sans point d’exclamation de début (**!**) ne peut pas être convertie en valeur.</span><span class="sxs-lookup"><span data-stu-id="7803e-124">In an XLL, a reference without a leading exclamation point (**!**) cannot be converted to a value.</span></span> <span data-ttu-id="7803e-125">Elle n’a aucune signification, car il n’existe pas de feuille macro actuelle.</span><span class="sxs-lookup"><span data-stu-id="7803e-125">It has no meaning because there is no current macro sheet.</span></span> <span data-ttu-id="7803e-126">Notez qu’un signe égal à ( ) est facultatif et **=** est omis dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="7803e-126">Note that a leading equals sign (**=**) is optional and is omitted in the next example.</span></span>
  
```C
int WINAPI evaluate_expression_example(void)
{
    wchar_t *expression = L"\022COUNT(!A1:IV65536)";
    XLOPER12 xExprText, xExprValue;
    xExprText.xltype = xltypeStr;
    xExprText.val.str = expression;
// Try to evaluate the formula.
    Excel12(xlfEvaluate, &xExprValue, 1, &xExprText);
// Attempt to convert the value to a string and display it in
// an alert dialog. Will fail if xExprValue is an error.
    Excel12(xlcAlert, 0, 1, &xExprValue);
// Not strictly necessary, as COUNT never returns a string
// but does no harm.
    Excel12(xlFree, 0, 1, &xExprValue);
    return 1;
}
```

<span data-ttu-id="7803e-127">Vous pouvez également utiliser la fonction **xlfEvaluate** pour récupérer l’ID d’inscription d’une fonction XLL à partir de son nom enregistré, qui peut ensuite être utilisé pour appeler cette fonction à l’aide de la fonction [xlUDF](xludf.md).</span><span class="sxs-lookup"><span data-stu-id="7803e-127">You can also use the **xlfEvaluate** function to retrieve the registration ID of an XLL function from its registered name, which can then be used to call that function using the [xlUDF function](xludf.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="7803e-128">Le nom enregistré peut être transmis directement à la **fonction xlUDF.**</span><span class="sxs-lookup"><span data-stu-id="7803e-128">The registered name can be passed directly to the **xlUDF** function.</span></span> <span data-ttu-id="7803e-129">Cela signifie que vous pouvez éviter d’avoir à évaluer le nom pour obtenir l’ID avant d’appeler **xlUDF**.</span><span class="sxs-lookup"><span data-stu-id="7803e-129">This means that you can avoid having to evaluate the name to get the ID before calling **xlUDF**.</span></span> <span data-ttu-id="7803e-130">Toutefois, si la fonction doit être appelée plusieurs fois, son appel à l’aide de l’ID d’inscription est plus rapide.</span><span class="sxs-lookup"><span data-stu-id="7803e-130">However, if the function is to be called many times, calling it by using the registration ID is faster.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7803e-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7803e-131">See also</span></span>

- [<span data-ttu-id="7803e-132">Feuille de calcul et évaluation des expressions Excel</span><span class="sxs-lookup"><span data-stu-id="7803e-132">Excel Worksheet and Expression Evaluation</span></span>](excel-worksheet-and-expression-evaluation.md)
- [<span data-ttu-id="7803e-133">Autorisation des interruptions utilisateur lors des opérations très longues</span><span class="sxs-lookup"><span data-stu-id="7803e-133">Permitting User Breaks in Lengthy Operations</span></span>](permitting-user-breaks-in-lengthy-operations.md)
- [<span data-ttu-id="7803e-134">Mise en route avec le Kit de d�veloppement logiciel XLL Excel 2013</span><span class="sxs-lookup"><span data-stu-id="7803e-134">Getting Started with the Excel XLL SDK</span></span>](getting-started-with-the-excel-xll-sdk.md)

