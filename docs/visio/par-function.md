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
ms.openlocfilehash: 925116363c147e5f976062e4bdf54dfbf74a4f81
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63376461"
---
# <a name="par-function"></a>Fonction PAR

Renvoie les  _coordonnées x,y_ d’un point dans le système de coordonnées du parent de la forme.
  
## <a name="syntax"></a>Syntaxe

PAR(***point*** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _point_ <br/> |Obligatoire  <br/> |**Number, Number** <br/> |Coordonnées du point dans le système de coordonnées de la forme actuelle |

## <a name="remarks"></a>Remarques

Dans Microsoft Visio, un point est une valeur unique qui représente une paire de coordonnées *x* et *y*. Si la forme fait partie d’un groupe, son parent est le groupe. Si la forme ne fait pas partie d’un groupe, son parent est la page.
  
## <a name="example"></a>Exemple

PAR(PNT(PinX,PinY))
  
Dans cette expression, PNT convertit un couple de coordonnées de la forme active en un point. La fonction PAR convertit ensuite le point en un couple de coordonnées par rapport au coin inférieur gauche de la page contenant la forme active.
  