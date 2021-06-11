---
title: Excel4v/Excel12v
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12v
- Excel4v
keywords:
- fonction excel12v [excel 2007],fonction Excel4v [Excel 2007]
localization_priority: Normal
ms.assetid: e3e96b98-c5a7-4625-95b6-a1e2d09c6d3d
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 11ab86a95dde2ad52840822b28ce4d74dd05d148
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414990"
---
# <a name="excel4vexcel12v"></a>Excel4v/Excel12v

 **S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Appelle une fonction de feuille de Microsoft Excel interne, une fonction ou une commande de feuille macro, ou une commande ou une fonction spéciale XLL uniquement, à partir d’une DLL, XLL ou ressource de code.
  
Toutes les versions récentes de Excel prise **en charge d’Excel4v.** À compter Excel 2007, **Excel12v** est pris en charge. 
  
Ces fonctions ne peuvent être appelées que si Excel a passé le contrôle à la DLL ou au XLL. Ils peuvent également être appelés lorsque Excel a passé le contrôle indirectement via un appel à Visual Basic pour Applications (VBA). Ils ne peuvent pas être appelés à un autre moment. Par exemple, ils ne peuvent pas être appelés pendant les appels à la fonction DllMain ou à d’autres moments où le système d’exploitation a appelé la DLL, ou à partir d’un thread créé par la DLL. 
  
Les fonctions Excel4 et [Excel12](excel4-excel12.md) acceptent leurs arguments en tant que liste de longueur variable sur la pile, tandis que les fonctions **Excel4v** et **Excel12v** acceptent leurs arguments en tant que tableau. À tous les autres égards, **Excel4** se comporte de la même manière **qu’Excel4v** et **Excel12** se comporte de la même manière **qu’Excel12v**.
  
```cs
int _cdecl Excel4v(int iFunction, LPXLOPER pxRes, int iCount, LPXLOPER rgx[]);
int _cdecl Excel12v(int iFunction, LPXLOPER12 pxRes, int iCount, LPXLOPER12 rgx[]);
```

## <a name="parameters"></a>Parameters

 _iFunction_ (**int**)
  
Nombre qui indique la commande, la fonction ou la fonction spéciale que vous voulez appeler. Pour obtenir la liste des valeurs  _iFunction_ valides, consultez la section Remarques suivante. 
  
 _pxRes_ (**LPXLOPER** ou **LPXLOPER12**)
  
Pointeur vers une **XLOPER** (dans le cas **d’Excel4v)** ou une **XLOPER12** (dans le cas **d’Excel12v)** qui conservera le résultat de la fonction évaluée.
  
 _iCount_ (**int**)
  
Nombre d’arguments ultérieurs qui seront transmis à la fonction. Dans les versions Excel jusqu’en 2003, ce nombre peut être n’importe quel nombre de 0 à 30. À compter Excel 2007, ce nombre peut être n’importe quel nombre entre 0 et 255.
  
 _rgx_ (**LPXLOPER []** ou **LPXLOPER12 []**)
  
Tableau qui contient les arguments de la fonction. Tous les arguments du tableau doivent être des pointeurs vers des valeurs **XLOPER** ou **XLOPER12.** 
  
## <a name="return-value"></a>Valeur renvoyée

Ces fonctions retournent les mêmes valeurs **qu’Excel4** et **Excel12**.
  
## <a name="remarks"></a>Remarques

Ces fonctions sont utiles lorsque le nombre d’arguments transmis à l’opérateur est variable. Par exemple, **Excel4v** et **Excel12v** sont utiles lorsque vous inscrivez des fonctions à l’aide de [xlfRegister](xlfregister-form-1.md) où le nombre total d’arguments dépend du nombre d’arguments pris par la fonction inscrite. **Excel4v et** **Excel12v** sont également utiles lorsque vous écrivez une fonction wrapper pour **Excel4** ou **Excel12**. Dans ce cas, vous devez convertir une liste d’arguments variables, comme normalement fourni à **Excel4** ou **Excel12,** en un argument de tableau unique de taille variable pour rappeler en Excel à l’aide d’Excel4v ou **Excel12v**. 
  
### <a name="example"></a>Exemple

Pour obtenir des exemples de code, consultez le code des fonctions **Excel** et **Excel12f** dans le SDK XLL Excel 2010, à l’emplacement suivant où vous avez installé le SDK : 
  
Samples\Framewrk\Framewrk.c
  
## <a name="see-also"></a>Voir aussi



[Excel4/Excel12](excel4-excel12.md)

