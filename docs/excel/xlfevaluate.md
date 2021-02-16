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
# <a name="xlfevaluate"></a>xlfEvaluate

 **S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Utilise l’analyseur et l’évaluateur de fonction Microsoft Excel pour évaluer toute expression qui pourrait être entrée dans une cellule de feuille de calcul.
  
```cs
Excel12(xlfEvaluate, LPXLOPER12 pxRes, 1, LPXLOPER12 pxFormulaText);
```

## <a name="parameters"></a>Paramètres

 _pxFormulaText (xltypeStr)_
  
Chaîne à évaluer. Un signe égal de premier plan (=) est facultatif. La chaîne peut être n’importe quel texte qui peut légalement être entré dans une feuille de calcul ou une cellule de feuille de macro.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

Renvoie le résultat de l’évaluation de la chaîne qui peut être l’un des types **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeNil**, **xltypeMulti**.
  
## <a name="remarks"></a>Remarques

La chaîne peut contenir uniquement des fonctions, et non des équivalents de commande. Cela équivaut à appuyer sur **F9 à** partir de la barre de formule. Si **xlfEvaluate** est appelé à partir d’une fonction de feuille de calcul XLL inscrite comme thread-safe, l’expression ne doit contenir que des fonctions thread-safe. 
  
L’utilisation principale de la fonction **xlfEvaluate** consiste à autoriser les DLL à rechercher la valeur affectée à un nom défini qui se trouve sur une feuille ou un nom masqué défini dans la DLL. Notez qu’au sein d’une DLL/XLL, un nom de feuille de calcul doit être précédé d’au moins un point d’exclamation (!) pour garantir qu’il est interprété comme externe à la DLL. Pour plus d’informations, voir [l’évaluation des noms et d’autres expressions de](evaluating-names-and-other-worksheet-formula-expressions.md)formule de feuille de calcul.
  
 **xlfEvaluate ne peut** pas être utilisé pour évaluer les références à une feuille externe qui n’est pas ouverte. 
  
## <a name="example"></a>Exemple

Cet exemple utilise **xlfEvaluate** pour forcer le texte « ! B38 " au contenu de la cellule B38. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`. Cette fonction appelle une macro de commande (**xlcAlert**) et ne fonctionne correctement qu’en cas d’appel à partir d’une feuille macro ou d’une commande macro.
  
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

## <a name="see-also"></a>Voir aussi

- [Fonctions XLM essentielles et utiles de l’API C](essential-and-useful-c-api-xlm-functions.md)

