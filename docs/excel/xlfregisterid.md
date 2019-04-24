---
title: xlfRegisterId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegisterId
keywords:
- fonction xlfRegisterId [Excel 2007]
localization_priority: Normal
ms.assetid: d34cf20c-a5cd-45fb-9dcb-d49eac2d99dd
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 05119226d0b6190a2c4b30846c03a59b5c3cd1d8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303877"
---
# <a name="xlfregisterid"></a>xlfRegisterId

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Peut être appelé à partir d'une DLL qui a elle-même été appelée par Microsoft Excel. Si une fonction est déjà inscrite, elle renvoie l'ID de Registre existant pour cette fonction sans la réenregistrer. Si une fonction n'est pas encore enregistrée, elle l'enregistre et renvoie l'ID de Registre résultant.
  
```cs
Excel12(xlfRegisterId, LPXLOPER12 pxRes, 3,     LPXLOPER12 pxModuleText, LPXLOPER12 pxProcedure, LPXLOPER12 pxTypeText);
```

## <a name="parameters"></a>Paramètres

_pxModuleText_ (**xltypeStr**)
  
Nom de la DLL contenant la fonction.
  
_pxProcedure_ (**xltypeStr** ou **xltypeNum**)
  
Si une chaîne, nom de la fonction à appeler. S'il s'agit d'un nombre, le numéro d'export ordinal de la fonction à appeler. Pour des fins de clarté et de robustesse, utilisez toujours le formulaire de chaîne.
  
_pxTypeText_ (**xltypeStr**)
  
Chaîne facultative spécifiant les types de tous les arguments de la fonction et le type de la valeur de retour de la fonction. Pour plus d'informations, reportez-vous à la section «Remarques». Cet argument peut être omis pour une DLL autonome qui définit **xlAutoRegister**.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

Renvoie l'ID de la fonction (**xltypeNum**), qui peut être utilisée dans les appels ultérieurs à **xlfUnregister**.
  
## <a name="remarks"></a>Remarques

Cette fonction est utile lorsque vous ne souhaitez pas vous soucier de la conservation d'un ID de Registre, mais vous en aurez besoin plus tard pour annuler l'inscription. Il est également utile pour affecter des menus, des outils et des boutons lorsque la fonction que vous souhaitez affecter se trouve dans une DLL.
  
Lorsqu'une fonction DLL ou XLL a été enregistrée avec un argument _pxFunctionText_ valide ayant été fourni à **XLFREGISTER**, son ID de Registre peut également être obtenu en transmettant la _pxFunctionText_ à la fonction **xlfEvaluate**.
  
## <a name="see-also"></a>Voir aussi

- [CASIER](xlfregister-form-1.md)
- [ANNULER l'inscription](xlfunregister-form-1.md)
- [Fonctions XLM essentielles et utiles de l’API C](essential-and-useful-c-api-xlm-functions.md)

