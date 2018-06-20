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
description: Renvoie l’arc sinus d’un nombre, par exemple, l’angle dont le sinus est nombre.
ms.openlocfilehash: e5ed8f9fc8c85ac4816fede03bfe6f6af5cbf5f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788054"
---
# <a name="asin-function"></a>ASIN, fonction

Renvoie l’arc sinus d’un nombre, par exemple, l’angle dont le sinus est *nombre* . 
  
## <a name="syntax"></a>Syntaxe

ASIN (** *numéro* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Sinus de l’angle.  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur entrée doit être dans la plage -1 < = *nombre* < = 1 ou un #NUM ! erreur est renvoyée. L’angle obtenu se situe dans la plage -PI/2 < = *angle* < = PI/2 radians (-90 < = *angle* < = 90 degrés). 
  
## <a name="example"></a>Exemple

ASIN(1)
  
Renvoie 90 deg
  

