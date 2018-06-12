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
description: Renvoie les coordonnées x, y d’un point dans le système de coordonnées du parent de la forme.
ms.openlocfilehash: a3f7afd3f9bc988a20526451a6d7d7081d27a2d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789221"
---
# <a name="par-function"></a>PAR, fonction

Renvoie les coordonnées _x, y_ d’un point dans le système de coordonnées du parent de la forme. 
  
## <a name="syntax"></a>Syntaxe

Valeur nominale (** *point* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _point_ <br/> |Obligatoire  <br/> |**Numéro,** <br/> |Coordonnées du point dans le système de coordonnées de la forme actuelle  <br/> |
   
## <a name="remarks"></a>Note

Dans Microsoft Visio, un point est une valeur single qui représente une paire de *x* et *y* -coordonnées. Si la forme est un groupe, son parent est le groupe. Si la forme n’est pas dans un groupe, son parent est la page. 
  
## <a name="example"></a>Exemple

PAR(Pnt(PinX,PinY)) 
  
Dans cette expression, PNT convertit un couple de coordonnées de la forme active en un point. La fonction PAR convertit ensuite le point en un couple de coordonnées par rapport au coin inférieur gauche de la page contenant la forme active. 
  

