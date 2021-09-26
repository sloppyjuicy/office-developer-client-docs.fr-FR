---
title: BLEND, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: c67b46bb-0eb2-f094-2870-c320bd488705
description: Combine deux couleurs dans la proportion spécifiée par le paramètre float.
ms.openlocfilehash: bacac9de24fed46f091ea3efaf9801740a918be2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613141"
---
# <a name="blend-function"></a>Fonction BLEND

Combine deux couleurs dans la proportion spécifiée par le _paramètre float._ 
  
## <a name="syntax"></a>Syntaxe

BLEND(** *color1* **, ** *color2* **, ** *float[0,1]* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _color1_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |L’index de couleurs Visio ou la valeur RVB de la première couleur.  <br/> |
| _color2_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |L’index de couleurs Visio ou la valeur RVB de la deuxième couleur.  <br/> |
| _float[0,1]_ <br/> |Obligatoire  <br/> |**Float** <br/> |Proportion de fusion respective de _color2_ et _color1._ Nombre réel entre 0 et 1 inclus.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

 **RGB**
  
## <a name="remarks"></a>Remarques

La couleur renvoyée est déterminée par les proportions relatives de fusion de _color2_ et _color1,_ respectivement, comme spécifié par le _paramètre float._ Par exemple, si  _float_ est de 0,25, la couleur renvoyée est composée de 75 % de  _color1_ et de 25 % de  _color2_. 
  
Une autre façon d’y penser est que la valeur  _float_ correspond au point le long de la gamme de couleurs de  _color1_ à  _color2_. Par conséquent, des nombres plus petits (proches de zéro) pour  _float_ produisent des fusions plus proches de  _color1_, tandis que les nombres plus grands (plus proches de 1) produisent des fusions plus proches de  _color2_.
  

