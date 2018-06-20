---
title: Évaluer les noms et les autres expressions de formule de feuille de calcul
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- évaluation de l’expression [excel 2007], feuilles de calcul [Excel 2007], d’évaluation de nom, évaluation des expressions [Excel 2007], l’évaluation de feuille de calcul des noms [Excel 2007], [Excel 2007], évaluation des noms [Excel 2007], évaluation, nom d’évaluation [Excel 2007] , chaînes [Excel 2007], convertissez les valeurs, fonction xlfEvaluate [Excel 2007], feuilles de calcul [Excel 2007], évaluation d’expression
localization_priority: Normal
ms.assetid: 2b23c75e-2a95-4f26-8714-2a73f5e326a7
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 9d726d89c859e2f7428b459971d5d13586f144e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782042"
---
# <a name="evaluating-names-and-other-worksheet-formula-expressions"></a>Évaluer les noms et les autres expressions de formule de feuille de calcul

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Une des fonctionnalités plus importantes Excel expose par le biais de l’API C est la possibilité de convertir une formule de chaîne qui peut être légalement entrée dans une feuille de calcul à une valeur ou un tableau de valeurs. Il est essentiel pour les fonctions XLL et commandes qui doivent lire le contenu de noms définis, par exemple. Cette capacité est exposée par le biais de la [fonction xlfEvaluate](xlfevaluate.md), comme illustré dans cet exemple.
  
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

Notez que lorsque vous évaluez un nom de feuille de calcul, sur son propre ou dans une formule, vous devez faire précéder le nom « ! », au moins. Dans le cas contraire, Excel tente de trouver le nom dans un espace de noms masqué réservé pour les DLL. Vous pouvez créer et supprimer des noms DLL masqués à l’aide de la [fonction xlfSetName](xlfsetname.md). Vous pouvez obtenir la définition de n’importe quel nom défini, qu’il s’agisse d’un nom DLL masqué ou une feuille de calcul, à l’aide de la fonction **xlfGetDef** . 
  
La spécification d’un nom de feuille de calcul complet prend la forme suivante :
  
`='C:\example folder\[Book1.xls]Sheet1'!Name`
  
Notez qu’Excel 2007 introduit un certain nombre de nouvelles extensions de fichier. Vous pouvez omettre le chemin d’accès, le nom du classeur et le nom de la feuille où il n’y a aucune ambiguïté entre les classeurs ouverts dans cette session d’Excel. 
  
L’exemple suivant calcule la formule `COUNT(A1:IV65536)` pour la feuille de calcul active et comment afficher le résultat. Notez la nécessité de préfixe avec l’adresse de la plage « ! », qui est conforme à la convention de référence de plage dans des feuilles macro XLM. Le XLM API C suit cette convention : 
  
- `=A1`Une référence à la cellule A1 de la feuille macro en cours. (Non définies pour XLL). 
  
- `=!A1`Une référence à la cellule A1 de la feuille active (ce qui peut être une feuille de calcul ou une feuille macro) 
  
- `=Sheet1!A1`Une référence à la cellule A1 de la feuille spécifiée, la feuille Sheet1 dans ce cas. 
  
- `=[Book1.xls]Sheet1!A1`Une référence à la cellule A1 dans la feuille spécifiée dans le classeur spécifié. 
  
Dans un XLL, une référence sans point d’exclamation principaux (**!**) ne peut pas être convertie en une valeur. Il n’a aucune signification car il n’existe aucune feuille macro en cours. Notez qu’un signe égal (**=**) est facultatif et est omis dans l’exemple suivant.
  
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

Vous pouvez également utiliser la fonction **xlfEvaluate** pour récupérer l’ID de l’enregistrement d’une fonction XLL à partir de son nom enregistré, qui peut ensuite être utilisé pour appeler cette fonction à l’aide de la [fonction xlUDF](xludf.md).
  
> [!NOTE]
> Le nom enregistré peut être passé directement à la fonction **xlUDF** . Cela signifie que vous pouvez éviter d’avoir à évaluer le nom pour obtenir l’ID avant d’appeler **xlUDF**. Toutefois, si la fonction est d’appeler plusieurs fois, appeler à l’aide de l’enregistrement QU'ID est plus rapide. 
  
## <a name="see-also"></a>Voir aussi

- [Feuille de calcul Excel et d’évaluation d’Expression](excel-worksheet-and-expression-evaluation.md)
- [Autorisation utilisateur sauts dans les opérations de longue durée](permitting-user-breaks-in-lengthy-operations.md)
- [Mise en route avec le Kit de d�veloppement logiciel XLL Excel 2013](getting-started-with-the-excel-xll-sdk.md)

