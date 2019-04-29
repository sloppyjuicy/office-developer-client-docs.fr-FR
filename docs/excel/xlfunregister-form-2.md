---
title: xlfUnregister (formulaire 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister (Form 2)
keywords:
- xlfUnregister [Excel 2007]
localization_priority: Normal
ms.assetid: 39c6eba7-ba41-4e7b-9a28-2b662378ff5a
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 8bf1151e1ba4c165e784b88dce80096a2eaa62de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419904"
---
# <a name="xlfunregister-form-2"></a>xlfUnregister (formulaire 2)

**S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Peut être appelée à partir d'une commande DLL ou XLL qui a elle-même été appelée par Microsoft Excel. Cela équivaut à appeler **Unregister** à partir d'une feuille macro XLM Excel. 
  
**xlfUnregister** peut être appelé sous deux formes: 
  
- Formulaire 1: annule l'inscription d'une commande ou d'une fonction individuelle.
    
- Formulaire 2: décharge et désactive un XLL.
    
Appelée dans le formulaire 2, cette fonction force une DLL ou une ressource de code à être déchargée entièrement. Elle annule l'inscription de toutes les fonctions d'une DLL, même si elles sont actuellement utilisées par une autre macro, quel que soit le nombre d'utilisations. Cette fonction appelle **xlAutoClose**, puis annule l'enregistrement de toutes les fonctions dans la dll.
  
```cs
Excel12(xlfUnregister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a>Paramètres

_pxModuleText_ (**xltypeStr**)
  
Nom de la DLL.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

Si elle réussit, renvoie la **valeur true** (**xltypeBool**). En cas d'échec, renvoie **false**.
  
## <a name="remarks"></a>Remarques

> [!NOTE] 
> N'appelez pas cette forme de la fonction à partir de votre implémentation de [xlAutoClose](xlautoclose.md) dans une tentative d'annulation de l'inscription de toutes les ressources de la dll avec un seul appel de fonction simple. Cela entraîne un appel récursif de **xlAutoClose** et un dépassement de capacité de la pile. 
  
### <a name="remember-to-delete-names"></a>N'oubliez pas de supprimer des noms

Si vous avez spécifié l'argument _pxFunctionText_ sur **xlfRegister**, lors de l'inscription des fonctions et commandes de la dll, vous devez supprimer explicitement les noms en appelant **xlfSetName** pour chacun d'eux, en omettant le second argument de sorte que le la fonction ne s'affiche plus dans l'Assistant fonction. Pour plus d’informations, reportez-vous à la rubrique [Problèmes connus concernant le développement de XLL Excel](known-issues-in-excel-xll-development.md).
  
## <a name="see-also"></a>Voir aussi

- [xlfRegister (formulaire 1)](xlfregister-form-1.md)
- [xlfRegisterId](xlfregisterid.md)
- [xlfUnregister (formulaire 1)](xlfunregister-form-1.md)
- [Fonctions XLM essentielles et utiles de l’API C](essential-and-useful-c-api-xlm-functions.md)

