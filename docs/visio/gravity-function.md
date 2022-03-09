---
title: GRAVITY, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251433
ms.localizationpriority: medium
ms.assetid: db80f147-71a0-0b23-bc7e-fe1915dfdd21
description: Calcule l’angle de rotation correct d’un bloc de texte pour la rotation de forme indiquée afin d’empêcher le texte de basculer vers le bas.
ms.openlocfilehash: 495965ef5747c21b079f84e6c8dfee68cbc5fe54
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63404123"
---
# <a name="gravity-function"></a>Fonction GRAVITY

Calcule l’angle de rotation correct d’un bloc de texte pour la rotation de forme indiquée afin d’empêcher le texte de basculer vers le bas.
  
## <a name="syntax"></a>Syntaxe

GRAVITY(***angle** _,[ _*_limit1_*_ ],[ _ *_limit2_** ])
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *angle* <br/> |Requis  <br/> |**String** <br/> | Angle de la forme. |
| *limit1* <br/> |Facultatif  <br/> |**Chaîne** <br/> |Première limite de rotation. La valeur par défaut est 90 degrés. |
| *limit2* <br/> |Facultatif  <br/> |**Chaîne** <br/> |Deuxième limite de rotation. La valeur par défaut est 270 degrés. |

### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

La fonction GRAVITY est généralement utilisée dans la cellule AngleTexte.
  
La valeur renvoyée est 180 degrés si l’argument *angle* est compris entre les valeurs spécifiées dans *limit1* et *limit2* ; sinon, la valeur renvoyée est 0 degré.
  
Tous les arguments sont automatiquement normalisés par la fonction à des valeurs comprises entre 0 et 360 degrés. Si un argument ne précise pas d’unités, les radians sont utilisés.
  
## <a name="example-1"></a>Exemple 1

GRAVITY(Angle)
  
Renvoie 180 degrés si  *l’angle*  est entre 90 et 270 degrés ; Sinon, renvoie 0 degré.
  
## <a name="example-2"></a>Exemple 2

GRAVITY(2)
  
Renvoie 180 degrés, car 2 radians est compris entre 90 et 270 degrés.
  
## <a name="example-3"></a>Exemple 3

GRAVITY(100 deg, 110 deg, 290 deg)
  
Renvoie 0 degré.
  
## <a name="example-4"></a>Exemple 4

GRAVITY(100 deg, 290 deg, 110 deg)
  
Renvoie 0 degré.
  