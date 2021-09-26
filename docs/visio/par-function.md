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
ms.openlocfilehash: b3ac20694b7ee2c4031c86a52f7c631685fb8b70
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627743"
---
# <a name="par-function"></a>Fonction PAR

Renvoie les  _coordonnées x,y_ d’un point dans le système de coordonnées du parent de la forme. 
  
## <a name="syntax"></a>Syntaxe

PAR(** *point* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _point_ <br/> |Obligatoire  <br/> |**Number, Number** <br/> |Coordonnées du point dans le système de coordonnées de la forme actuelle  <br/> |
   
## <a name="remarks"></a>Remarques

Dans Microsoft Visio, un point est une valeur unique qui représente une paire de coordonnées *x* et *y.* Si la forme fait partie d’un groupe, son parent est le groupe. Si la forme ne fait pas partie d’un groupe, son parent est la page. 
  
## <a name="example"></a>Exemple

PAR(PNT(PinX,PinY)) 
  
Dans cette expression, PNT convertit un couple de coordonnées de la forme active en un point. La fonction PAR convertit ensuite le point en un couple de coordonnées par rapport au coin inférieur gauche de la page contenant la forme active. 
  

