---
title: PNT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251480
ms.localizationpriority: medium
ms.assetid: d14a735c-0278-922f-7823-79adf6cb1e64
description: Renvoie le point représenté par les coordonnées x et y en tant que valeur unique.
ms.openlocfilehash: 6a51b1a897e6edf23d284101f7598148f700cfb8
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63404600"
---
# <a name="pnt-function"></a>Fonction PNT

Renvoie le point représenté par les coordonnées _x_ et _y_ en tant que valeur unique.
  
## <a name="syntax"></a>Syntaxe

PNT(***x,y*** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _x,y_ <br/> |Requis  <br/> |**Number, Number** <br/> |Coordonnées du point dans le système de coordonnées de la forme actuelle |

### <a name="return-value"></a>Valeur renvoyée

Pointer
  
## <a name="remarks"></a>Remarques

La conversion de coordonnées en points vous permet de modifier la géométrie d’une forme sans avoir à manipuler les coordonnées _x_ et _y_ séparément.
  
## <a name="example"></a>Exemple

PNT(PinX,PinY)
  
Renvoie le point représenté par AxeX et AxeY.
  