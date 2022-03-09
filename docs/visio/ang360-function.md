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
ms.openlocfilehash: 0b850379a4c1ed3c539bbceaec1a398982e2bfe2
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63376482"
---
# <a name="ang360-function"></a>Fonction ANG360

Normalise la plage d’un angle à 0 \<= \< résultat radians 2PI (0 \<= \< résultat 360 degrés).
  
## <a name="syntax"></a>Syntaxe

ANG360(***angle*** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *angle* <br/> |Obligatoire  <br/> |**Numérique** <br/> |Angle à normaliser. |

## <a name="remarks"></a>Remarques

Si l’*angle* n’est pas spécifié avec une unité de mesure d’angle, les radians sont utilisés. Si l’*angle* ne peut pas être converti en valeur, une erreur #VALEUR! est renvoyée.
  
## <a name="example-1"></a>Exemple 1

ANG360(395 deg)
  
Renvoie 35 deg
  
## <a name="example-2"></a>Exemple 2

ANG360(-9,8 rad)
  
Renvoie 2,7664 rad
  
## <a name="example-3"></a>Exemple 3

ANG360(45)
  
Renvoie 58,31 deg (1,0177 rad)
  