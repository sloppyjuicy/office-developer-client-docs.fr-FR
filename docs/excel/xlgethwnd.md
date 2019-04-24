---
title: xlGetHwnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetHwnd
keywords:
- fonction xlGetHwnd [Excel 2007]
localization_priority: Normal
ms.assetid: be33b097-812b-4f5c-81be-4d9673e95b0b
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: ab4ac1bc040ef2ea9bca182624111e03722c5200
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310065"
---
# <a name="xlgethwnd"></a>xlGetHwnd

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Renvoie le handle de fenêtre de la fenêtre Microsoft Excel de niveau supérieur.
  
```cs
Excel4(xlGetHwnd, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetHwnd, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a>Paramètres

Cette fonction n'a pas d'argument.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

Contient le handle de fenêtre (**xltypeInt**) dans le champ **Val. w** . 
  
## <a name="remarks"></a>Remarques

Cette fonction est utile pour écrire du code d'API Windows.
  
Lorsque vous appelez cette fonction à l'aide de [Excel4](excel4-excel12.md) ou [Excel4v](excel4v-excel12v.md), la variable de type entier XLOPER renvoyée est un nombre entier court 16 bits signé. Il ne peut contenir que les 16 bits de poids faible du handle Windows 32 bits. Pour trouver la partie haute, votre code doit parcourir toutes les fenêtres ouvertes à la recherche d'une correspondance avec la partie basse. À partir d'Excel 2007, la variable de type Integer de **XLOPER12** est un entier signé 32 bits et, par conséquent, le handle entier, ce qui supprime la nécessité d'itérer toutes les fenêtres ouvertes. 
  
### <a name="example"></a>Exemple

Voir le code de la [fonction fShowDialog](fshowdialog.md) dans `SAMPLES\GENERIC\GENERIC.C`.
  
## <a name="see-also"></a>Voir aussi

- [xlGetInst](xlgetinst.md)
- [Fonctions de l’API C à appeler à partir d’un fichier DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

