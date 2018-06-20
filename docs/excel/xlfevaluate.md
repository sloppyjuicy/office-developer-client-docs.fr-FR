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
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e468dc18b8f78f56acaa67c2f23dd53254088ad0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782216"
---
# <a name="xlfevaluate"></a>xlfEvaluate

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Utilise l’Analyseur de Microsoft Excel et évaluateur fonction pour évaluer une expression qui peut être saisie dans une cellule de feuille de calcul.
  
```cs
Excel12(xlfEvaluate, LPXLOPER12 pxRes, 1, LPXLOPER12 pxFormulaText);
```

## <a name="parameters"></a>Paramètres

 _pxFormulaText (xltypeStr)_
  
Chaîne à évaluer. Un signe de début égal (=) est facultatif. La chaîne peut être n’importe quel texte qui peut légalement être saisi dans une cellule de feuille de feuille de calcul ou de la macro.
  
## <a name="property-valuereturn-value"></a>Propriété valeur/valeur de retour

Renvoie le résultat de l’évaluation de la chaîne qui peut être un des types **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeNil**, **xltypeMulti**.
  
## <a name="remarks"></a>Remarques

La chaîne peut contenir uniquement des fonctions, pas les équivalents de commande. Elle équivaut à appuyer sur **F9** à partir de la barre de formule. Si **xlfEvaluate** est appelée à partir d’une fonction de feuille de calcul XLL qui a été enregistrée en tant que thread-safe, l’expression ne doit contenir que des fonctions de thread-safe. 
  
L’utilisation de la fonction **xlfEvaluate** principale consiste à autoriser les DLL déterminer la valeur attribuée à un nom défini qui est soit sur une feuille ou nom masqué définis dans la DLL. Notez que dans une DLL/XLL, un nom de feuille de calcul doit être précédé au moins un point d’exclamation ( !) pour vous assurer qu’elle est interprétée comme externe à la DLL. Pour plus d’informations, voir [évaluation des noms et autres Expressions de formule de feuille de calcul](evaluating-names-and-other-worksheet-formula-expressions.md).
  
 **xlfEvaluate** ne peut pas être utilisé pour évaluer les références à une feuille externe n’est pas ouvert. 
  
## <a name="example"></a>Exemple

Cet exemple utilise **xlfEvaluate** pour forcer le texte « ! B38 » pour le contenu de la cellule B38. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`. Cette fonction appelle une macro de commande (**xlcAlert**) et que l’opération correctement appelée à partir d’une feuille macro ou une commande de macro.
  
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

- [Fonctions XLM API C essentielles et utiles](essential-and-useful-c-api-xlm-functions.md)

