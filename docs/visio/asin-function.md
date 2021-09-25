---
title: ASIN, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251395
ms.localizationpriority: medium
ms.assetid: 7d917be4-65b1-002f-48cc-6d81916a1157
description: Renvoie l’arcsine d’un nombre, par exemple, l’angle dont le sinus est le nombre .
ms.openlocfilehash: d3cc3bb4afcb537f0234d4a5e51fc3fee00d809d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628863"
---
# <a name="asin-function"></a>Fonction ASIN

Renvoie l’arcsine d’un nombre, par exemple, l’angle dont le sinus est  *le nombre*  . 
  
## <a name="syntax"></a>Syntaxe

ASIN(***nombre*** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Sinus de l’angle.  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur d’entrée doit être dans la plage -1 <=  *nombre*  <= 1 ou une valeur #NUM! est renvoyée. L’angle obtenu se trouve dans la plage -PI/2 <=  *angle*  <= PI/2 radians (-90 <=  *angle*  <= 90 degrés). 
  
## <a name="example"></a>Exemple

ASIN(1)
  
Renvoie 90 deg
  

