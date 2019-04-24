---
title: CEILING, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251405
localization_priority: Normal
ms.assetid: 1a8d6d48-7ae3-5483-28d2-5b1706088a53
description: Arrondit un nombre en s'éloignant de 0 (zéro) à l'instance suivante de multiple. Si le multiple n'est pas spécifié, le nombre est arrondi de 0 à l'entier suivant.
ms.openlocfilehash: 449f17d1b68c116cccb2635723a3f6277d0ac2a9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337225"
---
# <a name="ceiling-function"></a>Fonction CEILING

Arrondit un nombre en s'éloignant de 0 (zéro) à l'instance suivante de _multiple_. Si le _multiple_ n'est pas spécifié, le nombre est arrondi de 0 à l'entier suivant. 
  
## <a name="syntax"></a>Syntaxe

PLAFOND (* * *nombre* * *, * * *multiple* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatoire  <br/> |**Number** <br/> |Nombre à arrondir.  <br/> |
| _sépar_ <br/> |Obligatoire  <br/> |**Number** <br/> |Multiple à arrondir.  <br/> |
   
## <a name="remarks"></a>Remarques

 _Number_ et _multiple_ doivent avoir les mêmes signes ou une #NUM! est renvoyée. Si _nombre_ ou _multiple_ ne peuvent pas être convertis en valeur, un #VALUE! est renvoyée. Si _nombre_ ou _multiple_ est 0, le résultat est 0. 
  
## <a name="example-1"></a>Exemple 1

PLAFOND (3.7)
  
Renvoie 4
  
## <a name="example-2"></a>Exemple 2

PLAFOND (-3,7)
  
Renvoie -4
  
## <a name="example-3"></a>Exemple 3

PLAFOND (3.7, 0,25)
  
Renvoie 3,75
  

