---
title: CEILING, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251405
ms.localizationpriority: medium
ms.assetid: 1a8d6d48-7ae3-5483-28d2-5b1706088a53
description: Arrondit un nombre de 0 (zéro) à l’instance suivante de plusieurs. Si plusieurs n’est pas spécifié, le nombre est arrondi de 0 à l’integer suivant.
ms.openlocfilehash: e544be99fe035e1394d55acb0af5a8ee78e7a06f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578115"
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
  

