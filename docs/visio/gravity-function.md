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
description: Calcule l’angle correct d’un bloc de texte de la rotation de la rotation de la forme indiquée empêcher le texte d’activation de haut en bas.
ms.openlocfilehash: 0d8b0160c7e7d63fb5a272219a2694d35e6e6b61
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19788733"
---
# <a name="gravity-function"></a>GRAVITY, fonction

Calcule l’angle correct d’un bloc de texte de la rotation de la rotation de la forme indiquée empêcher le texte d’activation de haut en bas.
  
## <a name="syntax"></a>Syntaxe

GRAVITY (** *angle* **, [** *limit1* **], [** *limit2* **]) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _angle_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> | Angle de la forme.  <br/> |
| _limit1_ <br/> |Facultatif  <br/> |**Chaîne** <br/> |Première limite de rotation. La valeur par défaut est 90 degrés.  <br/> |
| _limit2_ <br/> |Facultatif  <br/> |**Chaîne** <br/> |Deuxième limite de rotation. La valeur par défaut est 270 degrés.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Chaîne
  
## <a name="remarks"></a>Remarques

La fonction GRAVITY est généralement utilisée dans la cellule AngleTexte. 
  
La valeur renvoyée est 180 degrés si _angle_ est compris entre les valeurs spécifiées _dans limit1_ et _limit2_; dans le cas contraire, la valeur renvoyée est 0 degré.
  
Tous les arguments sont automatiquement normalisés par la fonction à des valeurs comprises entre 0 et 360 degrés. Si un argument ne précise pas d’unités, les radians sont utilisés. 
  
## <a name="example-1"></a>Exemple 1

GRAVITY(Angle)
  
Renvoie 180 degrés si *angle* est compris entre 90 et 270 degrés ; Sinon, renvoie 0 degré. 
  
## <a name="example-2"></a>Exemple 2

GRAVITY(2)
  
Renvoie 180 degrés, car 2 radians est compris entre 90 et 270 degrés.
  
## <a name="example-3"></a>Exemple 3

GRAVITY(100 deg, 110 deg, 290 deg)
  
Renvoie 0 degré.
  
## <a name="example-4"></a>Exemple 4

GRAVITY(100 deg, 290 deg, 110 deg)
  
Renvoie 0 degré.
  

