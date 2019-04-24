---
title: xlCoerce
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlCoerce
keywords:
- fonction xlCoerce [Excel 2007]
localization_priority: Normal
ms.assetid: 9d47c16c-a7e7-4998-b594-9cf001827b7b
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: d84839535d5eb913ca8a62d631238e3330683d0e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303961"
---
# <a name="xlcoerce"></a>xlCoerce

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Convertit un type de**XLOPER12** de type **XLOPER**/ en un autre, ou recherche des valeurs de cellule dans une feuille. 
  
```cs
Excel12(xlCoerce, LPXLOPER12 pxRes, 2, LPXLOPER12 pxSource, LPXLOPER12 pxDestType);
```

## <a name="parameters"></a>Paramètres

 _pxSource_
  
La source **XLOPER**/ **** source doit être convertie. 
  
 _pxDestType_ (**xltypeInt**)
  
(Facultatif). Masque de bits des types résultants que vous êtes prêt à accepter. Vous devez utiliser l'opérateur **** or au niveau du bit (|) pour spécifier plusieurs types possibles. Si vous ne spécifiez pas cet argument, les références à des cellules uniques sont converties en l'un des types de valeur **xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil** (si la cellule référencée est vide) et des références à des blocs de cellules sont converties en **xltypeMulti**. Cela rend **xlCoerce** le moyen le plus commode de rechercher des valeurs de cellule. 
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

Renvoie la valeur forcée (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil**ou **xltypeMulti**).
  
## <a name="remarks"></a>Remarques

 **xlCoerce** ne peut pas convertir vers ou à partir de **xltypeBigData** ou **xltypeFlow**. Le passage d'un type **xltypeMissing** ou **xltypeNil** en tant que _pxDestType_ revient à omettre l'argument. Dans certains cas, la conversion peut échouer. Par exemple, certaines chaînes ne peuvent pas être converties en nombres, contrairement à d'autres. 
  
Si un tableau ou une référence à plusieurs cellules est convertie en un seul type valeur, le résultat est la valeur de la cellule supérieure gauche ou du tableau.
  
## <a name="example"></a>Exemple

Le code suivant est disponible dans `\SAMPLES\EXAMPLE\EXAMPLE.C`. 
  
> [!NOTE]
> La fonction **xlcAlert** tente implicitement de convertir son argument en une chaîne de façon à ce que l'étape de forçage indiquée ici puisse être supprimée et **xInt** puisse être passé directement à **xlcAlert**. Comme **xlcAlert** est une macro de commande, ce code fonctionne uniquement lorsqu'il est appelé à partir d'une feuille macro. 
  
```cs
short WINAPI xlCoerceExample(short iVal)
{
   XLOPER12 xStr, xInt, xDestType;
   xInt.xltype = xltypeInt;
   xInt.val.w = iVal;
   xDestType.xltype = xltypeInt;
   xDestType.val.w = xltypeStr;
   Excel12f(xlCoerce, &xStr, 2, (LPXLOPER12)&xInt, (LPXLOPER12)&xDestType);
   Excel12f(xlcAlert, 0, 1, (LPXLOPER12)&xStr);
   Excel12f(xlFree, 0, 1, (LPXLOPER12)&xStr);
   return 1;
}
```

## <a name="see-also"></a>Voir aussi



[xlSet](xlset.md)


[Fonctions de l’API C à appeler à partir d’un fichier DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

