---
title: xlGetHwnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetHwnd
keywords:
- fonction xlgethwnd [excel 2007]
ms.localizationpriority: medium
ms.assetid: be33b097-812b-4f5c-81be-4d9673e95b0b
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 7698404927e11adec70341e791eacf389aafa4f0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557602"
---
# <a name="xlgethwnd"></a>xlGetHwnd

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Renvoie le handle de fenêtre de la fenêtre de niveau Microsoft Excel niveau supérieur.
  
```cs
Excel4(xlGetHwnd, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetHwnd, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a>Paramètres

Cette fonction n’a pas d’arguments.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

Contient le handle de fenêtre (**xltypeInt**) dans le **champ val.w.** 
  
## <a name="remarks"></a>Remarques

Cette fonction est utile pour écrire du code Windows API.
  
Lorsque vous appelez cette fonction à l’aide [d’Excel4](excel4-excel12.md) ou [d’Excel4v,](excel4v-excel12v.md)la variable d’integer XLOPER renvoyée est un int court signé 16 bits. Cette capacité ne peut contenir que les 16 bits faibles de la poignée de Windows 32 bits. Pour trouver la partie la plus élevée, votre code doit itérer dans toutes les fenêtres ouvertes à la recherche d’une correspondance avec la partie basse. À compter de Excel 2007, la variable entière de la **xlOPER12** est un entier signé 32 bits et contient donc la poignée entière, ce qui supprime la nécessité d’itérer toutes les fenêtres ouvertes. 
  
### <a name="example"></a>Exemple

Consultez le code de la [fonction fShowDialog dans](fshowdialog.md)  `SAMPLES\GENERIC\GENERIC.C` .
  
## <a name="see-also"></a>Voir aussi

- [xlGetInst](xlgetinst.md)
- [Fonctions de l’API C à appeler à partir d’un fichier DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

