---
title: xlGetHwnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetHwnd
keywords:
- fonction xlGetHwnd [excel 2007]
localization_priority: Normal
ms.assetid: be33b097-812b-4f5c-81be-4d9673e95b0b
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: a22365d6c945aaa5995e2c519c757a1a7515655a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782241"
---
# <a name="xlgethwnd"></a>xlGetHwnd

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Retourne le handle de fenêtre de la fenêtre Microsoft Excel de niveau supérieur.
  
```cs
Excel4(xlGetHwnd, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetHwnd, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a>Paramètres

Cette fonction ne comporte aucun argument.
  
## <a name="property-valuereturn-value"></a>Propriété valeur/valeur de retour

Contient le handle de fenêtre (**xltypeInt**) dans le champ **val.w** . 
  
## <a name="remarks"></a>Remarques

Cette fonction est utile pour l’écriture de code d’API Windows.
  
Lorsque vous appelez cette fonction à l’aide de [Excel4](excel4-excel12.md) ou [Excel4v](excel4v-excel12v.md), la variable de type entier XLOPER renvoyée est un entier signé 16 bits courte. Il s’agit des 16 bits de poids faibles de la poignée de Windows 32 bits. Pour trouver la partie haute, votre code doit itérer dans toutes les fenêtres ouvertes vous recherchez une correspondance avec la partie basse. À compter d’Excel 2007, la variable de type entier de la **XLOPER12** est un int 32 bits signé et par conséquent contient le handle entier, évite d’avoir à parcourir toutes les fenêtres ouvertes. 
  
### <a name="example"></a>Exemple

Voir le code de la [fonction fShowDialog](fshowdialog.md) dans `SAMPLES\GENERIC\GENERIC.C`.
  
## <a name="see-also"></a>Voir aussi

- [xlGetInst](xlgetinst.md)
- [Fonctions de l’API C qui peuvent être appelées uniquement à partir d’une DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

