---
title: ANG360, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251392
localization_priority: Normal
ms.assetid: 23e6899d-0a94-a7d8-8de2-091e0531f163
description: Normalise la plage d’un angle.
ms.openlocfilehash: 6916e50daad735843bf0a2a6361fb5b1b833e2ce
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160299"
---
# <a name="ang360-function"></a>Fonction ANG360

Normalise la plage d’un angle à 0 = résultat \< \< radians 2PI (0 = résultat \< \< 360 degrés).
  
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
  

