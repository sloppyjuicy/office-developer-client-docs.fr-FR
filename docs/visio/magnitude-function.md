---
title: MAGNITUDE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251461
ms.localizationpriority: medium
ms.assetid: 9f443687-9861-5f51-94c4-f056805f736b
description: Renvoie la magnitude du vecteur dont la montée est A et dont la run est B, multipliée par les constantes respectives constantA et constantB.
ms.openlocfilehash: c4d776b429fa1a290c0a0f88fdc1eff1a2510474
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63406196"
---
# <a name="magnitude-function"></a>Fonction MAGNITUDE

Renvoie la magnitude du vecteur dont la montée est _A_ et dont la run est _B_, multipliée par les constantes respectives _constantA_ et _constantB_.
  
## <a name="syntax"></a>Syntaxe

MAGNITUDE(***constantA** _, _*_A_*_, _*_constantB_*_, _ *_B_** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _constantA_ <br/> |Requis  <br/> |**Number** <br/> |Constante par laquelle multiplier la hauteur |
| _A_ <br/> |Requis  <br/> |**Number** <br/> |Hauteur |
| _constantB_ <br/> |Requis  <br/> |**Number** <br/> |Constante par laquelle multiplier la longueur |
| _B_ <br/> |Requis  <br/> |**Number** <br/> |Longueur |

## <a name="remarks"></a>Remarques

La fonction MAGNITUDE est calculée selon la formule suivante :
  
SQRT((constantA \* A)^2 + (constantB \* B)^2)
  
## <a name="example"></a>Exemple

MAGNITUDE(1; 3; 1; 4)
  
Renvoie 5.
  