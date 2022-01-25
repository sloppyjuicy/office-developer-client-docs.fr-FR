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
ms.localizationpriority: medium
ms.assetid: 6a719f04-b2d1-4f87-a227-be561cbd3e49
ms.openlocfilehash: 36e73e60a99ece68a078137c2c68bf0be5d78b4f
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62199026"
---
# <a name="funcfib"></a>FuncFib

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Exemple de fonction de feuille de calcul définie par l’utilisateur qui calcule le numéro Nth Fibonacci. Lorsque GENERIC.xll est chargé, il inscrit cette fonction afin qu’elle puisse être appelée à partir de la feuille de calcul.
  
```cs
LPXLOPER12 WINAPI FuncFib (LPXLOPER12 pxN);
```

## <a name="parameters"></a>Paramètres

 _pxN_ (**LPXLOPER12**)
  
Valeur de N pour laquelle le numéro Nth Fibonacci est requis.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

(**xltypeNum LPXLOPER12** en cas de réussite ou **xltypeErr dans le** cas contraire) 
  
Nième numéro Fibonacci.
  
## <a name="remarks"></a>Remarques

La fonction utilise une variable statique définie dans le bloc de fonctions comme valeur de retour **XLOPER12**. Cette fonction n’est pas thread-safe. Par exemple, cette fonction et toute fonction de feuille de calcul qui utilise cette stratégie pour renvoyer des **XLOPER** ou **XLOPER12** ne doivent pas être inscrites en tant que thread-safe à partir de Excel 2007.
  
### <a name="example"></a>Exemple

Voir `\SAMPLES\GENERIC\GENERIC.C` le code source pour cette fonction. 
  
## <a name="see-also"></a>Voir aussi



[Fonctions dans le fichier DLL générique](functions-in-the-generic-dll.md)

