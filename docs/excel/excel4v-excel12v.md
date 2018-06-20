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
- fonction Excel12v [excel 2007], fonction Excel4v [Excel 2007]
localization_priority: Normal
ms.assetid: e3e96b98-c5a7-4625-95b6-a1e2d09c6d3d
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 7ffa0bc3ae6222af1ecd7f65de66d026ea178c87
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782128"
---
# <a name="excel4vexcel12v"></a>Excel4v/Excel12v

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Appelle une fonction de feuille de calcul Microsoft Excel interne, la fonction de feuille macro ou commande, ou XLL seule fonction spéciale ou, à partir de DLL, XLL, ou de ressource de code.
  
Toutes les versions récentes d’Excel prennent en charge **Excel4v**. À compter d’Excel 2007, **Excel12v** est pris en charge. 
  
Ces fonctions peuvent être appelées uniquement lorsque Excel a réussi le contrôle à la DLL ou XLL. Ils peuvent également être appelées lorsque Excel a réussi le contrôle indirectement via un appel à Visual Basic pour Applications (VBA). Ils ne peuvent pas être appelées à tout moment. Par exemple, ils ne peuvent pas être appelées pendant un appel à la fonction DllMain ou autres heures lorsque le système d’exploitation a appelé la DLL ou d’un thread créé par la DLL. 
  
Les fonctions [Excel 4 et Excel12](excel4-excel12.md) acceptent leurs arguments comme une liste de longueur variable sur la pile, tandis que les fonctions **Excel4v** et **Excel12v** acceptent que les arguments comme un tableau. Dans tous les autres aspects **Excel4** se comporte comme **Excel4v**et **Excel12** se comporte comme **Excel12v**.
  
```cs
int _cdecl Excel4v(int iFunction, LPXLOPER pxRes, int iCount, LPXLOPER rgx[]);
int _cdecl Excel12v(int iFunction, LPXLOPER12 pxRes, int iCount, LPXLOPER12 rgx[]);
```

## <a name="parameters"></a>Paramètres

 _iFunction_ (**int**)
  
Un nombre qui indique la commande, une fonction ou une fonction spéciale que vous voulez appeler. Pour obtenir la liste des valeurs valides _iFunction_ , voir la section Remarques suivante. 
  
 _pxRes_ (**LPXLOPER** ou **LPXLOPER12**)
  
Pointeur vers un **XLOPER** (dans le cas d' **Excel4v**) ou une **XLOPER12** (dans le cas d' **Excel12v**) qui doit contenir le résultat de la fonction évaluée.
  
 _iCount_ (**int**)
  
Le nombre d’arguments suivants qui seront transmises à la fonction. Dans les versions d’Excel jusqu'à 2003 ce peut être n’importe quel nombre entre 0 et 30. À compter d’Excel 2007, il peut être n’importe quel nombre compris entre 0 et 255.
  
 _rgx_ (**[De LPXLOPER]** ou **[] LPXLOPER12**)
  
Tableau qui contient les arguments de la fonction. Tous les arguments du tableau doivent être des pointeurs aux valeurs **XLOPER** ou **XLOPER12** . 
  
## <a name="return-value"></a>Valeur renvoy�e

Ces fonctions renvoient les mêmes valeurs que **Excel4** et **Excel12**.
  
## <a name="remarks"></a>Remarques

Ces fonctions sont utiles lorsque le nombre d’arguments transmis à l’opérateur est variable. Par exemple, **Excel4v** et **Excel12v** sont utiles lorsque vous enregistrez des fonctions à l’aide de [xlfRegister](xlfregister-form-1.md) où le nombre d’arguments total dépend du nombre d’arguments effectuées par la fonction en cours d’enregistrement. **Excel4v** et **Excel12v** sont également utiles lorsque vous écrivez une fonction wrapper pour **Excel4** ou **Excel12**. Dans ces cas-là, vous devez convertir une liste d’arguments variable, comme vous le feriez normalement être fournis à **Excel4** ou **Excel12**, à un argument de tableau unique de la taille de la variable de rappeler dans Excel à l’aide de **Excel4v** ou **Excel12v**.
  
### <a name="example"></a>Exemple

Pour des exemples de code, voir le code pour les fonctions **Excel** et **Excel12f** dans le SDK XLL Excel 2010, à l’emplacement suivant, où vous avez installé le Kit de développement : 
  
Samples\Framewrk\Framewrk.c
  
## <a name="see-also"></a>Voir aussi



[Excel4/Excel12](excel4-excel12.md)

