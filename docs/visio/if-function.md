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
ms.openlocfilehash: 8364db9622d4e0432544d83c1265e2af0c4b33f6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612644"
---
# <a name="if-function"></a>Fonction IF

Renvoie  _valueiftrue si_  _logicalexpression_ a la valeur TRUE. Sinon, elle renvoie  _valueiffalse_.
  
## <a name="syntax"></a>Syntaxe

IF(** *logicalexpression* **, ** *valueiftrue* **, ** *valueiffalse* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _logicalexpression_ <br/> |Obligatoire  <br/> |**String** <br/> |Expression à évaluer.  <br/> |
| _valueiftrue_ <br/> |Obligatoire  <br/> |**Varie** <br/> |Valeur à renvoyer si  _logicalexpression_ est true.  <br/> |
| _valueiffalse_ <br/> |Obligatoire  <br/> |**Varie** <br/> | Valeur à renvoyer si  _logicalexpression_ est false.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Variables
  
## <a name="example"></a>Exemple

IF(Height \> 1.25 in,5,7)
  
Renvoie 5 si la hauteur de la forme est supérieure à 31,8 mm. Renvoie 7 si la hauteur de la forme est inférieure ou égale à 31,8 mm.
  

