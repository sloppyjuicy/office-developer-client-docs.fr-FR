---
title: BLEND, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: c67b46bb-0eb2-f094-2870-c320bd488705
description: Combine deux couleurs dans la proportion spécifiée par le paramètre float.
ms.openlocfilehash: a86f1d89a152b8a5bd3218977ddd78e2bc513e31
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62783619"
---
# <a name="blend-function"></a>Fonction BLEND

Combine deux couleurs dans la proportion spécifiée par le  _paramètre float_ . 
  
## <a name="syntax"></a>Syntaxe

BLEND(** *color1* **, ** *color2* **, ** *float[0,1]* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _color1_ <br/> |Requis  <br/> |**Numérique** <br/> |L’index de couleurs Visio ou la valeur RVB de la première couleur. |
| _color2_ <br/> |Requis  <br/> |**Numérique** <br/> |L’index de couleurs Visio ou la valeur RVB de la deuxième couleur. |
| _float[0,1]_ <br/> |Requis  <br/> |**Float** <br/> |Proportion de fusion respective des couleurs  _color2_ et  _color1_. Nombre réel entre 0 et 1 inclus. |
   
### <a name="return-value"></a>Valeur renvoyée

 **RGB**
  
## <a name="remarks"></a>Remarques

La couleur renvoyée est déterminée par les proportions relatives dans lesquelles la fusion  _de color2_ et  _color1_, respectivement, est déterminée par le paramètre  _float_ . Par exemple, si  _float_ est de 0,25, la couleur renvoyée est composée de 75 % de  _color1_ et de 25 % de  _color2_. 
  
Une autre façon d’y penser est que la valeur  _float_ correspond au point le long de la gamme de couleurs de  _color1_ à  _color2_. Par conséquent, des nombres plus petits (proches de zéro) pour les valeurs  _flottantes_ produisent des fusions plus proches de  _color1_, tandis que les plus grands nombres (plus proches de 1) produisent des fusions plus proches de  _color2_.
  

