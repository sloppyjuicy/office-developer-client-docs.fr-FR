---
title: FuncFib
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncFib
keywords:
- fonction funcfib [excel 2007]
localization_priority: Normal
ms.assetid: 6a719f04-b2d1-4f87-a227-be561cbd3e49
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 8d1c97ea57e968aaedffca6b37ded3d875e87413
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782124"
---
# <a name="funcfib"></a>FuncFib

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Exemple de fonction définie par l’utilisateur la feuille de calcul qui calcule le nombre Fibonacci nième. Lorsque GENERIC.xll est chargé, il enregistre cette fonction afin qu’elle peut être appelée à partir de la feuille de calcul.
  
```cs
LPXLOPER12 WINAPI FuncFib (LPXLOPER12 pxN);
```

## <a name="parameters"></a>Paramètres

 _pxN_ (**LPXLOPER12**)
  
La valeur de N pour lequel le nombre de Fibonacci nième est nécessaire.
  
## <a name="property-valuereturn-value"></a>Propriété valeur/valeur de retour

(**xltypeNum LPXLOPER12** en cas de réussite ou **xltypeErr** dans le cas contraire) 
  
Le nombre de Fibonacci nième.
  
## <a name="remarks"></a>Remarques

La fonction utilise une variable statique définie dans le bloc de fonction comme valeur de retour **XLOPER12**. Ce n’est pas thread-safe, et cette fonction et une fonction de feuille de calcul qui utilise cette stratégie pour le renvoi **XLOPER**ou **XLOPER12**, ne doivent pas être enregistrées en tant que thread-safe à compter d’Excel 2007.
  
### <a name="example"></a>Exemple

Voir `\SAMPLES\GENERIC\GENERIC.C` pour le code source pour cette fonction. 
  
## <a name="see-also"></a>Voir aussi



[Fonctions de la DLL générique](functions-in-the-generic-dll.md)

