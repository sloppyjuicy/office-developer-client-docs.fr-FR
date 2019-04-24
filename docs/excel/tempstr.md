---
title: TempStr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempStr
keywords:
- fonction TempStr [Excel 2007]
localization_priority: Normal
ms.assetid: b21b4868-babe-4255-9093-503172efa045
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 4ccb6f3c764371c35bac12c8c78fede54234a7d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310317"
---
# <a name="tempstr"></a>TempStr

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Fonction de bibliothèque d'infrastructure déConseillée qui crée un **XLOPER** temporaire contenant une chaîne d'octets **xltypeStr** . Elle prend une chaîne source se terminant par null comme entrée. Elle tente de remplacer le premier caractère de la chaîne fournie par la longueur de la chaîne suivante. Cette opération n'est pas toujours sûre: Microsoft Excel peut se bloquer si une chaîne en lecture seule a été transmise. 
  
```cs
LPXLOPER TempStr(LPSTR str);
```

## <a name="parameters"></a>Paramètres

 _str_
  
Pointeur vers la chaîne source se terminant par null. **TempStr** tronque les chaînes dont la taille est supérieure à 255 octets. 
  
## <a name="return-value"></a>Valeur renvoyée

Renvoie une chaîne **xltypeStr** contenant un pointeur vers la mémoire tampon de chaîne passée. 
  
## <a name="remarks"></a>Remarques

Cette méthode de création de chaînes temporaires est désormais déconseillée en faveur de la façon dont [TempStrConst et TempStr12](tempstrconst-tempstr12.md) fonctionnent. Ces fonctions allouent une nouvelle mémoire tampon et y copie la chaîne passée. Les chaînes d'entrée pour **TempStrConst** et **TempStr12** ne sont pas modifiées et sont déclarées comme **const**. En revanche, la chaîne d'entrée vers **TempStr** est modifiée et ne peut donc pas être déclarée comme **const**. Le premier caractère de la chaîne d'entrée est traité comme un espace pour un caractère de longueur et est remplacé par cette fonction.
  
## <a name="see-also"></a>Voir aussi



[Fonctions de la bibliothèque Framework](functions-in-the-framework-library.md)

