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
description: Calcule l’angle de rotation correct d’un bloc de texte pour la rotation de forme indiquée afin d’empêcher le texte de se retourner vers le bas.
ms.openlocfilehash: f8a564160fae9fe85b531631215de536a8c28406
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612709"
---
# <a name="gravity-function"></a>Fonction GRAVITY

Calcule l’angle de rotation correct d’un bloc de texte pour la rotation de forme indiquée afin d’empêcher le texte de se retourner vers le bas.
  
## <a name="syntax"></a>Syntaxe

GRAVITY(** *angle* **,[ ** *limit1* ** ],[ ** *limit2* ** ]) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _angle_ <br/> |Obligatoire  <br/> |**String** <br/> | Angle de la forme.  <br/> |
| _limit1_ <br/> |Facultatif  <br/> |**Chaîne** <br/> |Première limite de rotation. La valeur par défaut est 90 degrés.  <br/> |
| _limit2_ <br/> |Facultatif  <br/> |**Chaîne** <br/> |Deuxième limite de rotation. La valeur par défaut est 270 degrés.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

La fonction GRAVITY est généralement utilisée dans la cellule AngleTexte. 
  
La valeur renvoyée est de 180 degrés si  _l’angle_ se trouve entre les valeurs spécifiées par  _limit1_ et  _limit2_; Sinon, la valeur renvoyée est 0 degré.
  
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
  

