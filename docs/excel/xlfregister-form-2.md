---
title: xlfRegister (formulaire 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegister
keywords:
- fonction xlfregister [excel 2007]
ms.localizationpriority: medium
ms.assetid: 3ebbd775-f3d2-4ba7-8835-a5b38ad2267a
ms.openlocfilehash: f07d8a722e9df1e8b18d8b03f700b13bd3b037f5
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62199163"
---
# <a name="xlfregister-form-2"></a>xlfRegister (formulaire 2)

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Peut être appelée à partir d’une commande DLL ou XLL qui a elle-même été appelée par Microsoft Excel. Cela équivaut à appeler **REGISTER** à partir d’Excel feuille macro XLM. 
  
La **fonction xlfRegister** peut être appelée sous deux formes : 
  
- [xlfRegister (formulaire 1)](xlfregister-form-1.md): inscrit une commande ou une fonction individuelle.
    
- xlfRegister (formulaire 2) : charge et active une XLL.
    
Appelée dans le formulaire 2, cette fonction ne peut être utilisée que pour charger et activer une XLL contenant une procédure [xlAutoOpen.](xlautoopen.md) 
  
```cs
Excel12(xlfRegister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a>Paramètres

 _pxModuleText_ (**xltypeStr**)
  
Nom de la DLL à charger et à activer.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

Si elle réussit, cela renvoie le nom de la DLL (**xltypeStr**). Sinon, elle renvoie une #VALUE ! erreur.
  
## <a name="see-also"></a>Voir aussi



[Fonctions XLM essentielles et utiles de l’API C](essential-and-useful-c-api-xlm-functions.md)

