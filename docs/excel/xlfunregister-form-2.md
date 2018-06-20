---
title: xlfUnregister (formulaire 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister (Form 2)
keywords:
- xlfunregister [excel 2007]
localization_priority: Normal
ms.assetid: 39c6eba7-ba41-4e7b-9a28-2b662378ff5a
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e0154e380b65b8c57e7e96a98ef131e26b49e203
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782242"
---
# <a name="xlfunregister-form-2"></a>xlfUnregister (formulaire 2)

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Peut être appelée à partir d’une commande DLL ou XLL lui-même a été appelée par Microsoft Excel. Cela équivaut à appeler **Annuler l’inscription** d’une feuille de macro Excel XLM. 
  
**xlfUnregister** peut être appelée sous deux formes : 
  
- Formulaire 1 : Annule l’enregistrement d’une commande ou une fonction.
    
- Formulaire 2 : Décharge et désactive une solution XLL.
    
Appelé dans le formulaire 2, cette fonction force une DLL ou ressource de code pour être déchargé entièrement. Il annule l’inscription de toutes les fonctions dans une DLL, même si elles sont actuellement en cours d’utilisation par une autre macro, quel que soit le compteur d’utilisation. Cette fonction appelle **xlAutoClose**, puis annule l’enregistrement de toutes les fonctions de la DLL.
  
```cs
Excel12(xlfUnregister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a>Paramètres

_pxModuleText_ (**xltypeStr**)
  
Le nom de la DLL.
  
## <a name="property-valuereturn-value"></a>Propriété valeur/valeur de retour

Si l’opération réussit, renvoie **la valeur TRUE** (**xltypeBool**). En cas d’échec, renvoie **FALSE**.
  
## <a name="remarks"></a>Remarques

> [!NOTE] 
> N’appelez pas cette forme de la fonction à partir de votre implémentation de la [xlAutoClose](xlautoclose.md) lors d’une tentative d’annuler l’inscription de toutes les ressources de la DLL avec l’appel d’une fonction simple. Cela conduit à l’appel récursif de **xlAutoClose** et un dépassement. 
  
### <a name="remember-to-delete-names"></a>N’oubliez pas de supprimer des noms

Si vous spécifiez l’argument _pxFunctionText_ de **xlfRegister**, lors de l’inscription des fonctions et les commandes de la DLL, vous devez supprimer explicitement les noms en appelant **xlfSetName** pour chacun d’eux, en omettant le deuxième argument afin que la fonction n’apparaît plus dans l’Assistant fonction. Pour plus d�informations, consultez [Probl�mes connus concernant le d�veloppement de XLL Excel](known-issues-in-excel-xll-development.md).
  
## <a name="see-also"></a>Voir aussi

- [xlfRegister (formulaire 1)](xlfregister-form-1.md)
- [xlfRegisterId](xlfregisterid.md)
- [xlfUnregister (formulaire 1)](xlfunregister-form-1.md)
- [Fonctions XLM API C essentielles et utiles](essential-and-useful-c-api-xlm-functions.md)

