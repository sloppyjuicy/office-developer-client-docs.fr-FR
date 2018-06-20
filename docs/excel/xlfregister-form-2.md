---
title: xlfRegister (formulaire 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegister
keywords:
- fonction xlfRegister [excel 2007]
localization_priority: Normal
ms.assetid: 3ebbd775-f3d2-4ba7-8835-a5b38ad2267a
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: a535018e2b644966d183ba9ae862ce83670c9231
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782219"
---
# <a name="xlfregister-form-2"></a>xlfRegister (formulaire 2)

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Peut être appelée à partir d’une commande DLL ou XLL lui-même a été appelée par Microsoft Excel. Cela équivaut à appeler **l’Enregistrer** à partir d’une feuille de macro Excel XLM. 
  
La fonction **xlfRegister** peut être appelée sous deux formes : 
  
- [xlfRegister (formulaire 1)](xlfregister-form-1.md): enregistre une commande ou une fonction.
    
- xlfRegister (formulaire 2) : charges et Active une solution XLL.
    
Appelée dans le formulaire 2, cette fonction peut uniquement être utilisée pour charger et activer un XLL contenant une procédure [xlAutoOpen](xlautoopen.md) . 
  
```cs
Excel12(xlfRegister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a>Paramètres

 _pxModuleText_ (**xltypeStr**)
  
Le nom de la DLL à être chargé et activé.
  
## <a name="property-valuereturn-value"></a>Propriété valeur/valeur de retour

Si l’opération réussit, cela renvoie le nom de la DLL (**xltypeStr**). Dans le cas contraire, elle renvoie une #VALUE ! erreur.
  
## <a name="see-also"></a>Voir aussi



[Fonctions XLM API C essentielles et utiles](essential-and-useful-c-api-xlm-functions.md)

