---
title: Maintenant fonction (VisioShapeSheet)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251470
localization_priority: Normal
ms.assetid: 96cac1f6-cc17-466f-23d8-a9006e7de05f
description: Renvoie la valeur de date et l’heure actuelle.
ms.openlocfilehash: 387425369b1f1d6313502b3679a72cfd23038834
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789200"
---
# <a name="now-function-visioshapesheet"></a>Maintenant fonction (VisioShapeSheet)

Renvoie la valeur de date et l’heure actuelle.
  
## <a name="syntax"></a>Syntaxe

NOW ( )
  
### <a name="return-value"></a>Valeur renvoy�e

Datetime
  
## <a name="remarks"></a>Note

La fonction NOW est automatiquement recalculée toutes les minutes. 
  
## <a name="example-1"></a>Exemple 1

NOW( )
  
Renvoie la date et l’heure actuelles, 27/09/10 12:03:30, par exemple.
  
## <a name="example-2"></a>Exemple 2

FORMAT(NOW(),"jj MMM. aaaa hh:mm")
  
Renvoie la date et l’heure actuelles au format 27 sept. 2010 12:03.
  
## <a name="example-3"></a>Exemple 3

NOW()+2WE.
  
Renvoie la date et l’heure actuelles plus deux semaines, soit 10/11/10 12:03:30.
  

