---
title: GRAVITY, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251433
localization_priority: Normal
ms.assetid: db80f147-71a0-0b23-bc7e-fe1915dfdd21
description: Calcule l'angle de rotation correct d'un bloc de texte pour la rotation de forme indiquée de sorte que le texte ne soit pas renversé.
ms.openlocfilehash: 77c944d954292e231f8bacbe3c8a4433aad5d689
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429284"
---
# <a name="gravity-function"></a>Fonction GRAVITY

Calcule l'angle de rotation correct d'un bloc de texte pour la rotation de forme indiquée de sorte que le texte ne soit pas renversé.
  
## <a name="syntax"></a>Syntaxe

Gravité (* * *angle* * *, [* * *limite1* * *], [* * *limit2* * *]) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _angle_ <br/> |Obligatoire  <br/> |**String** <br/> | Angle de la forme.  <br/> |
| _limite1_ <br/> |Facultatif  <br/> |**Chaîne** <br/> |Première limite de rotation. La valeur par défaut est 90 degrés.  <br/> |
| _limit2_ <br/> |Facultatif  <br/> |**Chaîne** <br/> |Deuxième limite de rotation. La valeur par défaut est 270 degrés.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

La fonction GRAVITY est généralement utilisée dans la cellule AngleTexte. 
  
La valeur renvoyée est 180 degrees si _angle_ est compris entre les valeurs spécifiées par _limite1_ et _limit2_; Sinon, la valeur renvoyée est 0 degré.
  
Tous les arguments sont automatiquement normalisés par la fonction à des valeurs comprises entre 0 et 360 degrés. Si un argument ne précise pas d’unités, les radians sont utilisés. 
  
## <a name="example-1"></a>Exemple 1

GRAVITÉ (angle)
  
Renvoie 180 degrés si *angle* est compris entre 90 et 270 degrés; Sinon, renvoie 0 degré. 
  
## <a name="example-2"></a>Exemple 2

GRAVITÉ (2)
  
Renvoie 180 degrés, car 2 radians est compris entre 90 et 270 degrés.
  
## <a name="example-3"></a>Exemple 3

GRAVITY(100 deg, 110 deg, 290 deg)
  
Renvoie 0 degré.
  
## <a name="example-4"></a>Exemple 4

GRAVITY(100 deg, 290 deg, 110 deg)
  
Renvoie 0 degré.
  

