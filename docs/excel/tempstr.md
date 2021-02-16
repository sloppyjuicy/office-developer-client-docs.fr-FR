---
title: TempStr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempStr
keywords:
- fonction tempstr [excel 2007]
localization_priority: Normal
ms.assetid: b21b4868-babe-4255-9093-503172efa045
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4ccb6f3c764371c35bac12c8c78fede54234a7d6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418042"
---
# <a name="tempstr"></a>TempStr

 **S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Fonction de bibliothèque Deprecated Framework qui crée une **structure XLOPER** temporaire contenant une chaîne d’byte **xltypeStr.** Il prend une chaîne source terminée par null comme entrée. Il tente de faire en quoi le premier caractère de la chaîne fournie est réécrit par la longueur de la chaîne suivante. Ce n’est pas toujours une chose sûre : Microsoft Excel peut se crasher si une chaîne en lecture seule est passée. 
  
```cs
LPXLOPER TempStr(LPSTR str);
```

## <a name="parameters"></a>Paramètres

 _str_
  
Pointeur vers la chaîne source terminée par null. **TempStr** tronque les chaînes dont la durée est de plus de 255 octets. 
  
## <a name="return-value"></a>Valeur renvoyée

Renvoie une **chaîne xltypeStr** contenant un pointeur vers la mémoire tampon de chaîne transmise. 
  
## <a name="remarks"></a>Remarques

Cette façon de créer des chaînes temporaires est désormais dépréciée au profit de la façon dont [TempStrConst et TempStr12](tempstrconst-tempstr12.md) fonctionnent. Ces fonctions allouent une nouvelle mémoire tampon et y copient la chaîne transmise. Les chaînes d’entrée **pour TempStrConst** et **TempStr12** ne sont pas modifiées et sont donc déclarées comme **const**. En revanche, la chaîne d’entrée **à TempStr** est modifiée et ne peut donc pas être déclarée comme **const**. Le premier caractère de la chaîne d’entrée est traité comme un espace pour un caractère de longueur et est remplacé par cette fonction.
  
## <a name="see-also"></a>Voir aussi



[Fonctions de la bibliothèque Framework](functions-in-the-framework-library.md)

