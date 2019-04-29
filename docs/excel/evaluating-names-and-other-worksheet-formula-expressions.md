---
title: Évaluation des noms et d’autres expressions de formule dans les feuilles de calcul
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- évaluation d'expression [Excel 2007], feuilles de calcul [Excel 2007], évaluation de nom, expressions d'évaluation [Excel 2007], évaluation des noms de feuilles de calcul [Excel 2007], expressions [Excel 2007], évaluation, noms [Excel 2007], évaluation, évaluation de nom [Excel 2007] , chaînes [Excel 2007], conversion en valeurs, fonction xlfEvaluate [Excel 2007], feuilles de calcul [Excel 2007], évaluation de l'expression
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
# <a name="evaluating-names-and-other-worksheet-formula-expressions"></a>Évaluation des noms et d’autres expressions de formule dans les feuilles de calcul

**S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
L'une des fonctionnalités les plus importantes qu'Excel expose via l'API C est la possibilité de convertir toute formule de chaîne pouvant être légalement entrée dans une feuille de calcul en une valeur ou un tableau de valeurs. Ceci est essentiel pour les fonctions et commandes XLL qui doivent lire le contenu de noms définis, par exemple. Cette fonctionnalité est exposée par le biais de la [fonction xlfEvaluate](xlfevaluate.md), comme illustré dans cet exemple.
  
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

Notez que lorsque vous évaluez le nom d'une feuille de calcul, qu'il s'agisse de sa part ou d'une formule, vous devez faire précéder le nom de «!», au minimum. Dans le cas contraire, Excel essaie de trouver le nom dans un espace de noms masqué réservé pour les dll. Vous pouvez créer et supprimer des noms de DLL masqués à l'aide de la [fonction xlfSetName](xlfsetname.md). Vous pouvez obtenir la définition de n'importe quel nom défini, qu'il s'agisse d'un nom de DLL masqué ou d'un nom de feuille de calcul, à l'aide de la fonction **xlfGetDef** . 
  
La spécification complète d'un nom de feuille de calcul prend la forme suivante:
  
`='C:\example folder\[Book1.xls]Sheet1'!Name`
  
Notez qu'Excel 2007 a introduit un certain nombre de nouvelles extensions de fichiers. Vous pouvez omettre le chemin d'accès, le nom du classeur et le nom de la feuille où il n'y a aucune ambiguïté entre les classeurs ouverts dans cette session Excel. 
  
L'exemple suivant évalue la formule `COUNT(A1:IV65536)` de la feuille de calcul active et affiche le résultat. Remarque la nécessité de préfixer l'adresse de la plage avec «!», qui est cohérente avec la Convention de référence de plage sur les feuilles macro XLM. L'API C XLM suit la Convention suivante: 
  
- `=A1`Référence à la cellule a1 de la feuille macro active. (Non défini pour les XLL). 
  
- `=!A1`Référence à la cellule a1 de la feuille active (qui peut être une feuille de calcul ou une feuille macro) 
  
- `=Sheet1!A1`Référence à la cellule a1 de la feuille spécifiée, Sheet1 dans ce cas. 
  
- `=[Book1.xls]Sheet1!A1`Référence à la cellule a1 de la feuille spécifiée dans le classeur spécifié. 
  
Dans une XLL, une référence sans point d'exclamation de début (**!**) ne peut pas être convertie en valeur. Elle n'a aucune signification, car il n'existe pas de feuille macro active. Notez qu'un signe égal à gauche (**=**) est facultatif et n'est pas pris en compte dans l'exemple suivant.
  
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

Vous pouvez également utiliser la fonction **xlfEvaluate** pour récupérer l'ID d'enregistrement d'une fonction XLL à partir de son nom enregistré, qui peut ensuite être utilisé pour appeler cette fonction à l'aide de la [fonction xlUDF](xludf.md).
  
> [!NOTE]
> Le nom enregistré peut être passé directement à la fonction **xlUDF** . Cela signifie que vous pouvez éviter d'avoir à évaluer le nom pour obtenir l'ID avant d'appeler **xlUDF**. Toutefois, si la fonction doit être appelée plusieurs fois, son appel à l'aide de l'ID d'inscription est plus rapide. 
  
## <a name="see-also"></a>Voir aussi

- [Feuille de calcul et évaluation des expressions Excel](excel-worksheet-and-expression-evaluation.md)
- [Autorisation des interruptions utilisateur lors des opérations très longues](permitting-user-breaks-in-lengthy-operations.md)
- [Mise en route avec le Kit de d�veloppement logiciel XLL Excel 2013](getting-started-with-the-excel-xll-sdk.md)

