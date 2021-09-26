---
title: NOW Function (VisioShapeSheet)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251470
ms.localizationpriority: medium
ms.assetid: 96cac1f6-cc17-466f-23d8-a9006e7de05f
description: Renvoie la date et l’heure actuelles.
ms.openlocfilehash: 6ec4069334a4a11588d015b6b134926c75613188
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627862"
---
# <a name="now-function-visioshapesheet"></a>NOW Function (VisioShapeSheet)

Renvoie la date et l’heure actuelles.
  
## <a name="syntax"></a>Syntaxe

NOW ( )
  
### <a name="return-value"></a>Valeur renvoyée

Datetime
  
## <a name="remarks"></a>Remarques

La fonction NOW est automatiquement recalculée toutes les minutes. 
  
## <a name="example-1"></a>Exemple 1

NOW( )
  
Renvoie la date et l’heure actuelles, 27/09/10 12:03:30, par exemple.
  
## <a name="example-2"></a>Exemple 2

FORMAT(NOW(),"jj MMM. aaaa hh:mm")
  
Renvoie la date et l’heure actuelles au format 27 sept. 2010 12:03.
  
## <a name="example-3"></a>Exemple 3

NOW()+2EW.
  
Renvoie la date et l’heure actuelles plus deux semaines, soit 10/11/10 12:03:30.
  

