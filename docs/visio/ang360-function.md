---
title: ANG360, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251392
ms.localizationpriority: medium
ms.assetid: 23e6899d-0a94-a7d8-8de2-091e0531f163
description: Normalise la plage d’un angle.
ms.openlocfilehash: b94af0ea3d20c839f9bb314e042b2c19da0f0820
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603941"
---
# <a name="ang360-function"></a>Fonction ANG360

Normalise la plage d’un angle à 0 = résultat \< \< 2PI radians (0 \< = résultat \< 360 degrés).
  
## <a name="syntax"></a>Syntaxe

ANG360(***angle*** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _angle_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Angle à normaliser.  <br/> |
   
## <a name="remarks"></a>Remarques

Si  *l’angle*  n’est pas spécifié à l’aide d’unités angulaires, il est interprété comme des radians. Si  *l’angle*  ne peut pas être converti en valeur, un #VALUE! est renvoyée. 
  
## <a name="example-1"></a>Exemple 1

ANG360(395 deg)
  
Renvoie 35 deg
  
## <a name="example-2"></a>Exemple 2

ANG360(-9,8 rad)
  
Renvoie 2,7664 rad
  
## <a name="example-3"></a>Exemple 3

ANG360(45)
  
Renvoie 58,31 deg (1,0177 rad)
  

