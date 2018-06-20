---
title: xlCoerce
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlCoerce
keywords:
- fonction xlCoerce [excel 2007]
localization_priority: Normal
ms.assetid: 9d47c16c-a7e7-4998-b594-9cf001827b7b
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e0474b81a6d24663fe85303efc8fe2fd62cfdd82
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782222"
---
# <a name="xlcoerce"></a>xlCoerce

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Convertit un type de **XLOPER**/ **XLOPER12** vers un autre, ou recherche des valeurs de cellule dans une feuille. 
  
```cs
Excel12(xlCoerce, LPXLOPER12 pxRes, 2, LPXLOPER12 pxSource, LPXLOPER12 pxDestType);
```

## <a name="parameters"></a>Paramètres

 _pxSource_
  
La source **XLOPER**/ **XLOPER12** qui doit être convertie. 
  
 _pxDestType_ (**xltypeInt**)
  
(Facultatif). Un masque de bits des types qui en résulte, vous êtes prêt à accepter. Vous devez utiliser l’opérateur de bits **OR** (|) pour spécifier plusieurs types possibles. Si cet argument est omis, les références à des cellules uniques sont convertis à un des types de valeur **xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil** (si la cellule référencée est vide) et références aux blocs des cellules sont converties en **xltypeMulti**. Cela rend **xlCoerce** le meilleur moyen de rechercher des valeurs de cellules. 
  
## <a name="property-valuereturn-value"></a>Propriété valeur/valeur de retour

Renvoie la valeur forcée (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil**ou **xltypeMulti**).
  
## <a name="remarks"></a>Remarques

 Impossible de convertir **xlCoerce** vers ou depuis **xltypeBigData** ou **xltypeFlow**. En passant un type **xltypeMissing** ou **xltypeNil** comme _pxDestType_ équivaut à omettre l’argument. Conversion peut échouer dans certains cas. Par exemple, certaines chaînes ne peuvent pas être converties en nombres, tandis que d’autres personnes peuvent. 
  
Si une matrice ou une référence de cellule multiples est convertie en un type de valeur de type single, le résultat est la valeur de l’élément supérieur gauche cellule ou un tableau.
  
## <a name="example"></a>Exemple

Vous trouverez le code suivant dans `\SAMPLES\EXAMPLE\EXAMPLE.C`. 
  
> [!NOTE]
> La fonction **xlcAlert** implicitement tente de convertir une chaîne de son argument afin que l’étape du forçage de type indiqué ici en fait pu être supprimé, et **xInt** peut être passé directement à **xlcAlert**. **XlcAlert** est une macro de commande, ce code ne fonctionne correctement lorsqu’elle est appelée à partir d’une feuille macro. 
  
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


[Fonctions de l’API C qui peuvent être appelées uniquement à partir d’une DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

