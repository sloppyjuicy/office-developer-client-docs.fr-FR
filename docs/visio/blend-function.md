---
title: BLEND, fonction
manager: lindalu
ms.date: 03/09/2022
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: c67b46bb-0eb2-f094-2870-c320bd488705
description: Combine deux couleurs dans la proportion spécifiée par le paramètre float.
ms.openlocfilehash: f43d482fc9f921b7ca18f689f25a2fd1848a28c4
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63406147"
---
# <a name="blend-function"></a>Fonction BLEND

Combine deux couleurs dans la proportion spécifiée par le _paramètre float_ .
  
## <a name="syntax"></a>Syntaxe

BLEND(***color1** _, _*_color2_ **, **_float[0,1]_** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _color1_ <br/> |Requis  <br/> |**Numérique** <br/> |L’index de couleurs Visio ou la valeur RVB de la première couleur. |
| _color2_ <br/> |Requis  <br/> |**Numérique** <br/> |L’index de couleurs Visio ou la valeur RVB de la deuxième couleur. |
| _float[0,1]_ <br/> |Requis  <br/> |**Float** <br/> |La proportion de mélange pour _color2_ et _color1_. Nombre réel entre 0 et 1 inclus. |

### <a name="return-value"></a>Valeur renvoyée

 **RGB**
  
## <a name="remarks"></a>Remarques

La couleur renvoyée est déterminée par les proportions relatives du mélange de _color2_ et _color1_, comme spécifié par le paramètre _float_. Par exemple, si _float_ est 0.25, la couleur renvoyée est composée de 75 % de _color1_ et de 25 % de _color2_.
  
Une autre méthode consiste à ce que la valeur _float_ corresponde au point le long du spectre de couleurs de _color1_ à _color2_. Par conséquent, les nombres plus petits (plus proches de zéro) pour _float_ génèrent des mélanges plus proches de _color1_, alors que des nombres plus grands (plus proches de 1) génèrent des mélanges plus proches de _color2_.
  