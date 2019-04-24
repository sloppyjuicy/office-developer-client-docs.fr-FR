---
title: FuncFib
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncFib
keywords:
- fonction FuncFib [Excel 2007]
localization_priority: Normal
ms.assetid: 6a719f04-b2d1-4f87-a227-be561cbd3e49
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: fb8f0c12c27fb2c95007eb5006c1d8b90970f3ad
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310835"
---
# <a name="funcfib"></a>FuncFib

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Exemple de fonction de feuille de calcul définie par l'utilisateur qui calcule le nième nombre de Fibonacci. Lorsque GENERIC. xll est chargé, il enregistre cette fonction afin qu'elle puisse être appelée à partir de la feuille de calcul.
  
```cs
LPXLOPER12 WINAPI FuncFib (LPXLOPER12 pxN);
```

## <a name="parameters"></a>Paramètres

 _pxN_ (**LPXLOPER12**)
  
Valeur de N pour laquelle le nième nombre de Fibonacci est requis.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

(**XLTYPENUM LPXLOPER12** en cas de réussite ou **xltypeErr** ) 
  
Nième nombre de Fibonacci.
  
## <a name="remarks"></a>Remarques

La fonction utilise une variable statique définie dans le bloc de fonction comme valeur de retour **XLOPER12**. Cette fonction n'est pas thread-safe et, par conséquent, cette fonction, ainsi que n'importe quelle fonction de feuille de calcul qui utilise cette stratégie pour renvoyer des **XLOPER**s ou **XLOPER12**, ne doit pas être inscrite en tant que thread-safe en commençant dans Excel 2007.
  
### <a name="example"></a>Exemple

Voir `\SAMPLES\GENERIC\GENERIC.C` pour obtenir le code source de cette fonction. 
  
## <a name="see-also"></a>Voir aussi



[Fonctions dans le fichier DLL générique](functions-in-the-generic-dll.md)

