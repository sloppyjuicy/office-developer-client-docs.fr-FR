---
title: xlfRegister (formulaire 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegister
keywords:
- fonction xlfRegister [Excel 2007]
localization_priority: Normal
ms.assetid: 3ebbd775-f3d2-4ba7-8835-a5b38ad2267a
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 66af741456ab763ef346a8777429f0ae1be77c11
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416040"
---
# <a name="xlfregister-form-2"></a>xlfRegister (formulaire 2)

 **S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Peut être appelée à partir d'une commande DLL ou XLL qui a elle-même été appelée par Microsoft Excel. Cela équivaut à appeler **Register** à partir d'une feuille macro XLM Excel. 
  
La fonction **xlfRegister** peut être appelée sous deux formes: 
  
- [xlfRegister (formulaire 1)](xlfregister-form-1.md): inscrit une commande ou une fonction individuelle.
    
- xlfRegister (formulaire 2): charge et active un XLL.
    
Appelée dans le formulaire 2, cette fonction ne peut être utilisée que pour charger et activer une XLL contenant une procédure [xlAutoOpen](xlautoopen.md) . 
  
```cs
Excel12(xlfRegister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a>Paramètres

 _pxModuleText_ (**xltypeStr**)
  
Nom de la DLL à charger et à activer.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

Si elle réussit, cette propriété renvoie le nom de la DLL (**xltypeStr**). Dans le cas contraire, elle renvoie une #VALUE! «.
  
## <a name="see-also"></a>Voir aussi



[Fonctions XLM essentielles et utiles de l’API C](essential-and-useful-c-api-xlm-functions.md)

