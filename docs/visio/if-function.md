---
title: IF, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251442
ms.localizationpriority: medium
ms.assetid: 66771ad3-0fb3-68ff-81da-d1162d37c05a
description: Renvoie valueiftrue si logicalexpression a la valeur TRUE. Sinon, elle renvoie valueiffalse.
ms.openlocfilehash: 62b04006b78265be3823d783933c49e160b348d5
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63405169"
---
# <a name="if-function"></a>Fonction IF

Renvoie _valueiftrue si_ _logicalexpression_ a la valeur TRUE. Sinon, elle renvoie _valueiffalse_.
  
## <a name="syntax"></a>Syntaxe

IF(***logicalexpression** _, _*_valueiftrue_*_, _ *_valueiffalse_** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _logicalexpression_ <br/> |Requis  <br/> |**String** <br/> |Expression à évaluer. |
| _valueiftrue_ <br/> |Requis  <br/> |**Varie** <br/> |Valeur à renvoyer si l’expression _logicalexpression_ a la valeur true. |
| _valueiffalse_ <br/> |Requis  <br/> |**Varie** <br/> | Valeur à renvoyer si l’expression _logicalexpression_ a la valeur true. |

### <a name="return-value"></a>Valeur renvoyée

Variables
  
## <a name="example"></a>Exemple

IF(Height \> 1.25 in,5,7)
  
Renvoie 5 si la hauteur de la forme est supérieure à 31,8 mm. Renvoie 7 si la hauteur de la forme est inférieure ou égale à 31,8 mm.
  