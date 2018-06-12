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
description: Renvoie le point représenté par les coordonnées x et y sous la forme d’une valeur unique.
ms.openlocfilehash: be00f7d5ae55f70407e35eca43881a6d3f70ec13
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789311"
---
# <a name="pnt-function"></a>PNT, fonction

Renvoie le point représenté par les coordonnées _x_ et _y_ sous la forme d’une valeur unique. 
  
## <a name="syntax"></a>Syntaxe

PNT (** *x, y* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _x, y_ <br/> |Obligatoire  <br/> |**Numéro,** <br/> |Coordonnées du point dans le système de coordonnées de la forme actuelle  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Point
  
## <a name="remarks"></a>Note

Conversion des coordonnées en points vous permet de modifier la géométrie d’une forme sans devoir manipuler *x* et *y* -coordonne séparément. 
  
## <a name="example"></a>Exemple

Pnt(PinX,PinY) 
  
Renvoie le point représenté par AxeX et AxeY. 
  

