---
title: PNT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251480
localization_priority: Normal
ms.assetid: d14a735c-0278-922f-7823-79adf6cb1e64
description: Renvoie le point représenté par les coordonnées x et y en tant que valeur unique.
ms.openlocfilehash: c0a12aa18f4c766ea1f5b0fa1d827804d766713c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435711"
---
# <a name="pnt-function"></a>Fonction PNT

Renvoie le point représenté par les coordonnées  _x_ et  _y_ en tant que valeur unique. 
  
## <a name="syntax"></a>Syntaxe

PNT(** *x,y* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _x,y_ <br/> |Obligatoire  <br/> |**Number, Number** <br/> |Coordonnées du point dans le système de coordonnées de la forme actuelle  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Pointer
  
## <a name="remarks"></a>Remarques

La conversion de coordonnées en points vous permet de modifier la géométrie d’une forme sans avoir à manipuler les coordonnées  *x*  et  *y*  séparément. 
  
## <a name="example"></a>Exemple

PNT(PinX,PinY) 
  
Renvoie le point représenté par AxeX et AxeY. 
  

