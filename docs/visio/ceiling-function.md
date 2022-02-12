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
ms.openlocfilehash: be017d3e414e74e74d315144d001df13e9120fbf
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62771747"
---
# <a name="ceiling-function"></a>Fonction CEILING

Arrondit un nombre de 0 (zéro) à l’instance suivante de  _plusieurs_. Si  _plusieurs_ n’est pas spécifié, le nombre est arrondi de 0 à l’integer suivant. 
  
## <a name="syntax"></a>Syntaxe

CEILING(** *number* **, ** *multiple* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Requis  <br/> |**Number** <br/> |Nombre à arrondir. |
| _multiple_ <br/> |Requis  <br/> |**Number** <br/> |Multiple à arrondir. |
   
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
  

