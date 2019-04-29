---
title: FLOOR, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251423
localization_priority: Normal
ms.assetid: 6788bc96-cc86-5f21-781f-67274e7f605a
description: Arrondit un nombre vers 0 (zéro), l'entier suivant ou l'occurrence suivante de multiple.
ms.openlocfilehash: 7a16a77a990180f34dd7a5706c24ec3232438467
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439897"
---
# <a name="floor-function"></a>Fonction FLOOR

Arrondit un nombre vers 0 (zéro), l'entier suivant ou l'occurrence suivante de _multiple_.
  
## <a name="syntax"></a>Syntaxe

PLANCHER (* * *nombre* * *, * * *multiple* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatoire  <br/> |**Number** <br/> |Nombre à arrondir.  <br/> |
| _sépar_ <br/> |Obligatoire  <br/> |**Number** <br/> |Multiple vers lequel arrondir.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Nombre
  
## <a name="remarks"></a>Remarques

Si le _multiple_ n'est pas spécifié, le nombre est arrondi à l'entier supérieur de 0. 
  
 _Number_ et _multiple_ doivent avoir les mêmes signes ou une #NUM! est renvoyée. Si _nombre_ ou _multiple_ ne peuvent pas être convertis en valeur, un #VALUE! est renvoyée. Si _nombre_ ou _multiple_ est 0, le résultat est 0. 
  
## <a name="example-1"></a>Exemple 1

PLANCHER (3.7)
  
Renvoie 3.
  
## <a name="example-2"></a>Exemple 2

PLANCHER (-3,7)
  
Renvoie -3.
  
## <a name="example-3"></a>Exemple 3

PLANCHER (3.7, 0,5)
  
Renvoie 3,5.
  

