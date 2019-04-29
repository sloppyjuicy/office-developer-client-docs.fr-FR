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
- fonction Excel12v [Excel 2007], fonction Excel4v [Excel 2007]
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
  
Appelle une fonction de feuille de calcul Microsoft Excel interne, une fonction de feuille de macro ou une commande, ou une fonction ou une commande spéciale XLL uniquement, à partir d'une ressource DLL, XLL ou de code.
  
Toutes les versions récentes d'Excel prennent en charge **Excel4v**. À partir d'Excel 2007, **Excel12v** est pris en charge. 
  
Ces fonctions ne peuvent être appelées que lorsqu'Excel a passé le contrôle à la DLL ou au XLL. Elles peuvent également être appelées lorsqu'Excel a passé le contrôle indirectement via un appel à Visual Basic pour applications (VBA). Elles ne peuvent pas être appelées à un autre moment. Par exemple, ils ne peuvent pas être appelés pendant les appels à la fonction DllMain ou à d'autres moments où le système d'exploitation a appelé la DLL ou à partir d'un thread créé par la DLL. 
  
Les fonctions [Excel4 et Excel12](excel4-excel12.md) acceptent leurs arguments sous la forme d'une liste de longueur variable dans la pile, tandis que les fonctions **Excel4v** et **Excel12v** acceptent leurs arguments sous forme de tableau. À tous les autres égards, **Excel4** se comporte de la même manière que **Excel4v**, et **Excel12** se comporte de la même manière que **Excel12v**.
  
```cs
int _cdecl Excel4v(int iFunction, LPXLOPER pxRes, int iCount, LPXLOPER rgx[]);
int _cdecl Excel12v(int iFunction, LPXLOPER12 pxRes, int iCount, LPXLOPER12 rgx[]);
```

## <a name="parameters"></a>Paramètres

 _IFunction_ (**int**)
  
Nombre qui indique la commande, la fonction ou la fonction spéciale que vous souhaitez appeler. Pour obtenir la liste des valeurs _IFunction_ valides, reportez-vous à la section notes suivantes. 
  
 _pxRes_ (**LPXLOPER** ou **LPXLOPER12**)
  
Pointeur vers une **XLOPER** (dans le cas de **Excel4v**) ou un **XLOPER12** (dans le cas de **Excel12v**) qui contiendra le résultat de la fonction évaluée.
  
 _iCount_ (**int**)
  
Nombre d'arguments suivants qui seront transmis à la fonction. Dans les versions d'Excel jusqu'à 2003, il peut s'agir d'un nombre compris entre 0 et 30. À partir d'Excel 2007, il peut s'agir de n'importe quel nombre compris entre 0 et 255.
  
 _RGX_ (**LPXLOPER []** ou **LPXLOPER12 []**)
  
Tableau qui contient les arguments de la fonction. Tous les arguments dans le tableau doivent être des pointeurs vers les valeurs **XLOPER** ou **XLOPER12** . 
  
## <a name="return-value"></a>Valeur renvoyée

Ces fonctions renvoient les mêmes valeurs que **Excel4** et **Excel12**.
  
## <a name="remarks"></a>Remarques

Ces fonctions sont utiles lorsque le nombre d'arguments transmis à l'opérateur est variable. Par exemple, **Excel4v** et **Excel12v** sont utiles lorsque vous enregistrez des fonctions à l'aide de [xlfRegister](xlfregister-form-1.md) , où le nombre d'arguments total dépend du nombre d'arguments pris par la fonction en cours d'enregistrement. **Excel4v** et **Excel12v** sont également utiles lorsque vous écrivez une fonction de wrapper pour **Excel4** ou **Excel12**. Dans ce cas, vous devez convertir une liste d'arguments de variable, comme normalement fourni à **Excel4** ou **Excel12**, à un seul argument de tableau de taille variable pour rappeler dans Excel à l'aide de **Excel4v** ou de **Excel12v**.
  
### <a name="example"></a>Exemple

Pour des exemples de code, reportez-vous au code pour les fonctions **Excel** et **EXCEL12F** dans le kit de développement XLL Excel 2010, à l'emplacement suivant où vous avez installé le kit de développement logiciel (SDK): 
  
Samples\Framewrk\Framewrk.c
  
## <a name="see-also"></a>Voir aussi



[Excel4/Excel12](excel4-excel12.md)

