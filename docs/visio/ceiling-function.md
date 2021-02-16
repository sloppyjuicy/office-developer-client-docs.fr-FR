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
description: Arrondit un nombre de 0 (zéro) à l’instance suivante de plusieurs. Si plusieurs n’est pas spécifié, le nombre est arrondi de 0 à l’integer suivant.
ms.openlocfilehash: 449f17d1b68c116cccb2635723a3f6277d0ac2a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404126"
---
# <a name="ceiling-function"></a>Fonction CEILING

Arrondit un nombre de 0 (zéro) à l’instance suivante de  _plusieurs_. Si  _plusieurs_ n’est pas spécifié, le nombre est arrondi de 0 à l’integer suivant. 
  
## <a name="syntax"></a>Syntaxe

CEILING(** *number* **, ** *multiple* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatoire  <br/> |**Number** <br/> |Nombre à arrondir.  <br/> |
| _multiple_ <br/> |Obligatoire  <br/> |**Number** <br/> |Multiple à arrondir.  <br/> |
   
## <a name="remarks"></a>Remarques

 _Les_  _nombres et multiples_ doivent avoir les mêmes signes ou une #NUM ! est renvoyée. Si un  _nombre ou_  _plusieurs ne_ peut pas être converti en valeur, un #VALUE! est renvoyée. Si le  _nombre ou_  _plusieurs est_ 0, le résultat est 0. 
  
## <a name="example-1"></a>Exemple 1

CEILING(3.7)
  
Renvoie 4
  
## <a name="example-2"></a>Exemple 2

CEILING(-3,7)
  
Renvoie -4
  
## <a name="example-3"></a>Exemple 3

CEILING(3.7, 0.25)
  
Renvoie 3,75
  

