---
title: xlCoerce
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlCoerce
keywords:
- fonction xièreerce [excel 2007]
ms.localizationpriority: medium
ms.assetid: 9d47c16c-a7e7-4998-b594-9cf001827b7b
ms.openlocfilehash: 9b8c561150c34f56393710eab35b3701d8983d81
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62199688"
---
# <a name="xlcoerce"></a>xlCoerce

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Convertit un type de **XLOPER** /  **XLOPER12** en un autre ou recherche des valeurs de cellule sur une feuille. 
  
```cs
Excel12(xlCoerce, LPXLOPER12 pxRes, 2, LPXLOPER12 pxSource, LPXLOPER12 pxDestType);
```

## <a name="parameters"></a>Paramètres

 _pxSource_
  
 /  **XlOPER12** source à convertir. 
  
 _pxDestType_ (**xltypeInt**)
  
(Facultatif). Masque de bits des types résultants que vous êtes prêt à accepter. Vous devez utiliser l’opérateur **OR** au niveau du bit ( | ) pour spécifier plusieurs types possibles. Si cet argument est omis, les références à des cellules individuelles sont converties en un des types de valeur **xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil** (si la cellule référencé est vide) et les références aux blocs de cellules sont converties en **xltypeMulti**. Cela rend **xlCoerce** le moyen le plus pratique de rechercher des valeurs de cellule. 
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

Renvoie la valeur contrainte (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil** ou **xltypeMulti**).
  
## <a name="remarks"></a>Remarques

 **xlCoerce ne peut** pas convertir vers ou à partir **de xltypeBigData ou** **xltypeFlow**. Passer un type **xltypeMissing** ou **xltypeNil** en tant que  _pxDestType_ équivaut à omettre l’argument. La conversion peut échouer dans certains cas. Par exemple, certaines chaînes ne peuvent pas être converties en nombres, tandis que d’autres le peuvent. 
  
Si un tableau ou une référence à plusieurs cellules est converti en un seul type de valeur, le résultat est la valeur de la cellule supérieure gauche ou de l’élément de tableau.
  
## <a name="example"></a>Exemple

Le code suivant se trouve dans  `\SAMPLES\EXAMPLE\EXAMPLE.C` . 
  
> [!NOTE]
> La fonction **xlcAlert** tente implicitement de convertir son argument en chaîne afin que l’étape de contrainte indiquée ici puisse en fait être supprimée et **que xInt** puisse être transmis directement à **xlcAlert**. Comme **xlcAlert est** une macro de commande, ce code fonctionne correctement uniquement lorsqu’il est appelé à partir d’une feuille macro. 
  
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

