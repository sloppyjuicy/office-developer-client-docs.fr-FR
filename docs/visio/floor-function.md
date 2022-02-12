---
title: FLOOR, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251423
ms.localizationpriority: medium
ms.assetid: 6788bc96-cc86-5f21-781f-67274e7f605a
description: Arrondit un nombre à 0 (zéro), à l’integer suivant ou à l’instance suivante de plusieurs.
ms.openlocfilehash: 778fa7ab50ec4d1ae9cb886f88b3c9bfcda1b4a7
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62787281"
---
# <a name="floor-function"></a>Fonction FLOOR

Arrondit un nombre à 0 (zéro), à l’integer suivant ou à l’instance suivante de  _plusieurs_.
  
## <a name="syntax"></a>Syntaxe

FLOOR(** *number* **, ** *multiple* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Requis  <br/> |**Number** <br/> |Nombre à arrondir. |
| _multiple_ <br/> |Requis  <br/> |**Number** <br/> |Multiple vers lequel arrondir. |
   
### <a name="return-value"></a>Valeur renvoyée

Nombre
  
## <a name="remarks"></a>Remarques

Si  _plusieurs_ n’est pas spécifié, le nombre est arrondi de 0 à l’integer suivant. 
  
 _Les_  _nombres et multiples_ doivent avoir les mêmes signes ou une #NUM ! est renvoyée. Si un  _nombre ou_  _plusieurs ne_ peut pas être converti en valeur, un #VALUE! est renvoyée. Si le  _nombre ou_  _plusieurs est_ 0, le résultat est 0. 
  
## <a name="example-1"></a>Exemple 1

FLOOR(3.7)
  
Renvoie 3.
  
## <a name="example-2"></a>Exemple 2

FLOOR(-3.7)
  
Renvoie -3.
  
## <a name="example-3"></a>Exemple 3

FLOOR(3.7, 0.5)
  
Renvoie 3,5.
  

