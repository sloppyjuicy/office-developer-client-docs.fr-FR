---
title: Évaluation des noms et d’autres expressions de formule dans les feuilles de calcul
manager: lindalu
ms.date: 01/22/2022
ms.audience: Developer
ms.topic: overview
keywords:
- expression evaluation [excel 2007],worksheets [Excel 2007], name evaluation,evaluating expressions [Excel 2007],evaluating worksheet names [Excel 2007],expressions [Excel 2007], evaluating,names [Excel 2007], evaluating,name evaluation [Excel 2007],strings [Excel  2007], converting to values,xlfEvaluate function [Excel 2007],worksheets [Excel 2007], expression evaluation
ms.localizationpriority: medium
ms.assetid: 2b23c75e-2a95-4f26-8714-2a73f5e326a7
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a21a6b1926cc31eadb11ad6573539a466d0d2625
ms.sourcegitcommit: 2411ec8262cd0ed92f8a072fb53b51e3e496d49e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/24/2022
ms.locfileid: "62180298"
---
# <a name="evaluating-names-and-other-worksheet-formula-expressions"></a>Évaluation des noms et d’autres expressions de formule dans les feuilles de calcul

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio
  
L’une des fonctionnalités les plus importantes exposées par Excel via l’API C est la possibilité de convertir toute formule de chaîne qui peut légalement être entrée dans une feuille de calcul en une valeur ou un tableau de valeurs. Cela est essentiel pour les fonctions et commandes XLL qui doivent lire le contenu des noms définis, par exemple. Cette capacité est exposée par le biais de la fonction [xlfEvaluate,](xlfevaluate.md)comme illustré dans cet exemple.
  
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

Notez que lorsque vous évaluez un nom de feuille de calcul, soit seul, soit dans une formule, vous devez au moins faire précéder le nom par « ! ». Sinon, Excel tente de trouver le nom dans un espace de noms masqué réservé aux DLL. Vous pouvez créer et supprimer des noms de DLL masqués à l’aide de la [fonction xlfSetName](xlfsetname.md). Vous pouvez obtenir la définition de n’importe quel nom défini, qu’il s’agit d’un nom DLL masqué ou d’un nom de feuille de calcul, à l’aide de la fonction **xlfGetDef.**
  
La spécification complète d’un nom de feuille de calcul se présente comme suit :
  
`='C:\example folder\[Book1.xls]Sheet1'!Name`
  
Notez que Excel 2007 a introduit un certain nombre de nouvelles extensions de fichier. Vous pouvez omettre le chemin d’accès, le nom du Excel feuille et le nom de la feuille sans ambiguïté.
  
L’exemple suivant évalue la formule de la feuille de calcul active et `COUNT(A1:IV65536)` affiche le résultat. Notez la nécessité de préfixer l’adresse de la plage par « ! » qui est cohérente avec la convention de référence de plage sur les feuilles macro XLM. La XME de l’API C suit cette convention :
  
- `=A1` Référence à la cellule A1 de la feuille macro actuelle. (Non défini pour les XL).
  
- `=!A1` Référence à la cellule A1 de la feuille active (feuille de calcul ou feuille macro)
  
- `=Sheet1!A1` Référence à la cellule A1 de la feuille spécifiée, Sheet1 dans ce cas.

- `=[Book1.xls]Sheet1!A1` Référence à la cellule A1 de la feuille spécifiée dans le livre de travail spécifié.
  
Dans une XLL, une référence sans point d’exclamation de début (**!**) ne peut pas être convertie en valeur. Elle n’a aucune signification, car il n’existe pas de feuille macro actuelle. Notez qu’un signe de début égal à ( ) est facultatif et **=** est omis dans l’exemple suivant.
  
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

Vous pouvez également utiliser la fonction **xlfEvaluate** pour récupérer l’ID d’inscription d’une fonction XLL à partir de son nom enregistré, qui peut ensuite être utilisé pour appeler cette fonction à l’aide de la fonction [xlUDF](xludf.md).
  
> [!NOTE]
> Le nom enregistré peut être transmis directement à la **fonction xlUDF.** Cela signifie que vous pouvez éviter d’avoir à évaluer le nom pour obtenir l’ID avant d’appeler **xlUDF**. Toutefois, si la fonction doit être appelée plusieurs fois, son appel à l’aide de l’ID d’inscription est plus rapide.
  
## <a name="see-also"></a>Voir aussi

- [Feuille de calcul et évaluation des expressions Excel](excel-worksheet-and-expression-evaluation.md)
- [Autorisation des interruptions utilisateur lors des opérations très longues](permitting-user-breaks-in-lengthy-operations.md)
- [Mise en route avec le Kit de d�veloppement logiciel XLL Excel 2013](getting-started-with-the-excel-xll-sdk.md)
