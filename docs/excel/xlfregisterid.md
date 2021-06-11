---
title: xlfRegisterId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegisterId
keywords:
- fonction xlfregisterid [excel 2007]
localization_priority: Normal
ms.assetid: d34cf20c-a5cd-45fb-9dcb-d49eac2d99dd
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 05119226d0b6190a2c4b30846c03a59b5c3cd1d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420058"
---
# <a name="xlfregisterid"></a>xlfRegisterId

**S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Peut être appelée à partir d’une DLL qui a elle-même été appelée par Microsoft Excel. Si une fonction est déjà inscrite, elle renvoie l’ID de registre existant pour cette fonction sans l’réinsister. Si une fonction n’est pas encore inscrite, elle l’inscrit et renvoie l’ID de registre résultant.
  
```cs
Excel12(xlfRegisterId, LPXLOPER12 pxRes, 3,     LPXLOPER12 pxModuleText, LPXLOPER12 pxProcedure, LPXLOPER12 pxTypeText);
```

## <a name="parameters"></a>Parameters

_pxModuleText_ (**xltypeStr**)
  
Nom de la DLL contenant la fonction.
  
_pxProcedure_ (**xltypeStr** ou **xltypeNum**)
  
S’il s’agit d’une chaîne, le nom de la fonction à appeler. S’il s’agit d’un nombre, le numéro d’exportation ordinal de la fonction à appeler. Pour plus de clarté et de robustesse, utilisez toujours la forme de chaîne.
  
_pxTypeText_ (**xltypeStr**)
  
Chaîne facultative spécifiant les types de tous les arguments de la fonction et le type de la valeur de retour de la fonction. Pour plus d’informations, voir la section « Remarques ». Cet argument peut être omis pour une DLL (XLL) autonome définissant **xlAutoRegister**.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

Renvoie l’ID de registre de la fonction (**xltypeNum**), qui peut être utilisé dans les appels ultérieurs **à xlfUnregister**.
  
## <a name="remarks"></a>Remarques

Cette fonction est utile lorsque vous ne souhaitez pas vous soucier de la maintenance d’un ID de registre, mais vous en avez besoin ultérieurement pour l’inscription. Il est également utile pour affecter des menus, des outils et des boutons lorsque la fonction que vous souhaitez affecter se trouve dans une DLL.
  
Lorsqu’une fonction DLL ou XLL a été inscrite avec un argument  _pxFunctionText_ valide ayant été fourni à **xlfRegister**, son ID de registre peut également être obtenu en passant  _le pxFunctionText_ à la fonction **xlfEvaluate**.
  
## <a name="see-also"></a>Voir aussi

- [REGISTER](xlfregister-form-1.md)
- [UNREGISTER](xlfunregister-form-1.md)
- [Fonctions XLM essentielles et utiles de l’API C](essential-and-useful-c-api-xlm-functions.md)

