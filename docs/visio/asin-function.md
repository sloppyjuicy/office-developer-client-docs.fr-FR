---
title: ASIN, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251395
ms.localizationpriority: medium
ms.assetid: 7d917be4-65b1-002f-48cc-6d81916a1157
description: Renvoie l’arcsine d’un nombre, par exemple, l’angle dont le sinus est le nombre .
ms.openlocfilehash: 4759525e21dfab0a48f086dca5c8823544da3a58
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62783683"
---
# <a name="asin-function"></a>Fonction ASIN

Renvoie l’arcsine d’un nombre, par exemple, l’angle dont le sinus est  *le nombre*  . 
  
## <a name="syntax"></a>Syntaxe

ASIN(***number*** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Requis  <br/> |**Numérique** <br/> |Sinus de l’angle. |
   
## <a name="remarks"></a>Remarques

La valeur d’entrée doit être dans la plage -1 <=  *nombre*  <= 1 ou une valeur #NUM! est renvoyée. L’angle obtenu se trouve dans la plage -PI/2 <=  *angle*  <= PI/2 radians (-90 <=  *angle*  <= 90 degrés). 
  
## <a name="example"></a>Exemple

ASIN(1)
  
Renvoie 90 deg
  

