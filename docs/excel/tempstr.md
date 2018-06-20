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
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: ce9399168d5b94d10481d2d0b5b69dd2e1d1d2e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782201"
---
# <a name="tempstr"></a>TempStr

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Obsolète fonction bibliothèque Framework qui crée un temporaire **XLOPER** contenant une chaîne d’octets **xltypeStr** . Il prend une chaîne source se termine par null comme entrée. Il essaie de remplacer le premier caractère de la chaîne fournie avec la longueur de la chaîne suivante. Ce n’est pas toujours une chose à faire fiable : Microsoft Excel peut s’interrompre si reçoit une chaîne en lecture seule. 
  
```cs
LPXLOPER TempStr(LPSTR str);
```

## <a name="parameters"></a>Paramètres

 _Str_
  
Pointeur vers la chaîne source terminée. **TempStr** tronque les chaînes qui sont supérieures à 255 octets. 
  
## <a name="return-value"></a>Valeur renvoy�e

Renvoie une chaîne **xltypeStr** contenant un pointeur vers la mémoire tampon de chaîne transmise. 
  
## <a name="remarks"></a>Remarques

Cette méthode de création de chaînes temporaires est désormais déconseillée en faveur de la façon dans les deux [TempStrConst et TempStr12](tempstrconst-tempstr12.md) de travail. Ces fonctions allouer une nouvelle mémoire tampon et copiez la chaîne transmise. Les chaînes d’entrée pour **TempStrConst** et **TempStr12** ne sont pas modifiées et sont donc déclarés comme **const**. En revanche, la chaîne d’entrée **TempStr** est modifiée et donc ne peut pas être déclarée comme **const**. Le premier caractère de la chaîne d’entrée est traité comme un espace pour un caractère de longueur et est remplacé par cette fonction.
  
## <a name="see-also"></a>Voir aussi



[Fonctions de la bibliothèque Framework](functions-in-the-framework-library.md)

