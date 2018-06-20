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
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: cd401393b7465442cef9342b942a27456871c68b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782232"
---
# <a name="xlfregisterid"></a>xlfRegisterId

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Peut être appelée à partir d’une DLL lui-même a été appelée par Microsoft Excel. Si une fonction est déjà enregistrée, elle renvoie l’identificateur de Registre existant de la fonction sans réinscription il. Si une fonction n’est pas encore inscrit, il enregistre et renvoie l’identificateur de Registre qui en résulte.
  
```cs
Excel12(xlfRegisterId, LPXLOPER12 pxRes, 3,     LPXLOPER12 pxModuleText, LPXLOPER12 pxProcedure, LPXLOPER12 pxTypeText);
```

## <a name="parameters"></a>Paramètres

_pxModuleText_ (**xltypeStr**)
  
Le nom de la DLL contenant la fonction.
  
_pxProcedure_ (**xltypeStr** ou **xltypeNum**)
  
Si aucune chaîne, le nom de la fonction à appeler. Si un nombre, la propriété ordinal exporter nombre de la fonction à appeler. Pour plus de clarté et robustesse, utilisez toujours la forme de chaîne.
  
_pxTypeText_ (**xltypeStr**)
  
Chaîne facultative spécifiant les types de tous les arguments de la fonction et le type de la valeur de retour de la fonction. Pour plus d’informations, voir la section « Remarques ». Cet argument peut être omis pour une autonome DLL (XLL) définition **xlAutoRegister**.
  
## <a name="property-valuereturn-value"></a>Propriété valeur/valeur de retour

Renvoie l’identificateur de Registre de la fonction (**xltypeNum**), qui peut être utilisée dans les appels suivants à **xlfUnregister**.
  
## <a name="remarks"></a>Remarques

Cette fonction est utile lorsque vous ne souhaitez pas à se soucier de maintenir un ID de Registre, mais vous devez une version ultérieure pour annuler l’inscription. Il est également utile pour l’affectation à des outils, des menus et des boutons lorsque la fonction que vous voulez attribuer est dans une DLL.
  
Lorsqu’une fonction DLL ou XLL a été enregistrée avec un argument valide _pxFunctionText_ ayant été fourni à **xlfRegister**, son ID registre peut également être obtenu en transmettant le _pxFunctionText_ à la fonction **xlfEvaluate**.
  
## <a name="see-also"></a>Voir aussi

- [INSCRIRE](xlfregister-form-1.md)
- [ANNULER L’INSCRIPTION](xlfunregister-form-1.md)
- [Fonctions XLM API C essentielles et utiles](essential-and-useful-c-api-xlm-functions.md)

