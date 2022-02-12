---
title: PAR, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251477
ms.localizationpriority: medium
ms.assetid: 9caf424d-cb70-8f1a-b984-64cf776bdfb4
description: Renvoie les coordonnées x,y d’un point dans le système de coordonnées du parent de la forme.
ms.openlocfilehash: 5300ad10e48f65d1061e505499a4ee8ae8599ac3
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62775405"
---
# <a name="par-function"></a>Fonction PAR

Renvoie les  _coordonnées x,y_ d’un point dans le système de coordonnées du parent de la forme. 
  
## <a name="syntax"></a>Syntaxe

PAR(** *point* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _point_ <br/> |Requis  <br/> |**Number, Number** <br/> |Coordonnées du point dans le système de coordonnées de la forme actuelle |
   
## <a name="remarks"></a>Remarques

Dans Microsoft Visio, un point est une valeur unique qui représente une paire de coordonnées *x* et *y*. Si la forme fait partie d’un groupe, son parent est le groupe. Si la forme ne fait pas partie d’un groupe, son parent est la page. 
  
## <a name="example"></a>Exemple

PAR(PNT(PinX,PinY)) 
  
Dans cette expression, PNT convertit un couple de coordonnées de la forme active en un point. La fonction PAR convertit ensuite le point en un couple de coordonnées par rapport au coin inférieur gauche de la page contenant la forme active. 
  

