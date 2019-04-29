---
title: ASIN, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251395
localization_priority: Normal
ms.assetid: 7d917be4-65b1-002f-48cc-6d81916a1157
description: Renvoie l'arcsinus d'un nombre, par exemple, l'angle dont le sinus est nombre.
ms.openlocfilehash: a7585dc07053466203f11cc04ce249ceb62fbda0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432820"
---
# <a name="asin-function"></a>Fonction ASIN

Renvoie l'arcsinus d'un nombre, par exemple, l'angle dont le sinus est *nombre* . 
  
## <a name="syntax"></a>Syntaxe

ASIN (* * *nombre* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Sinus de l’angle.  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur d'entrée doit être comprise entre-1 < = *nombre* < = 1, ou une #NUM! est renvoyée. L'angle obtenu se trouve dans la plage-PI/2 < = *angle* _LT_ = pi/2 radians (-90 < = *angle* < = 90 degrés). 
  
## <a name="example"></a>Exemple

ASIN (1)
  
Renvoie 90 deg
  

