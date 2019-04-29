---
title: PAR, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251477
localization_priority: Normal
ms.assetid: 9caf424d-cb70-8f1a-b984-64cf776bdfb4
description: Renvoie les coordonnées x, y d'un point dans le système de coordonnées du parent de la forme.
ms.openlocfilehash: 4e7517c4210db31f1c3f5dc8bf98185b6f4104aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414507"
---
# <a name="par-function"></a>Fonction PAR

Renvoie les coordonnées _x, y_ d'un point dans le système de coordonnées du parent de la forme. 
  
## <a name="syntax"></a>Syntaxe

PAR (* * *point* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _virgule_ <br/> |Obligatoire  <br/> |**Number, Number** <br/> |Coordonnées du point dans le système de coordonnées de la forme actuelle  <br/> |
   
## <a name="remarks"></a>Remarques

Dans Microsoft Visio, un point est une valeur unique qui représente une paire de coordonnées *x* et *y* . Si la forme fait partie d’un groupe, son parent est le groupe. Si la forme ne fait pas partie d’un groupe, son parent est la page. 
  
## <a name="example"></a>Exemple

PAR (PNT (PinX, PinY)) 
  
Dans cette expression, PNT convertit un couple de coordonnées de la forme active en un point. La fonction PAR convertit ensuite le point en un couple de coordonnées par rapport au coin inférieur gauche de la page contenant la forme active. 
  

