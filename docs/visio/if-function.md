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
ms.openlocfilehash: ada10a0ec50a890515dc3a56f645006c7bb7a55e
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62775715"
---
# <a name="if-function"></a>Fonction IF

Renvoie  _valueiftrue si_  _logicalexpression_ a la valeur TRUE. Sinon, elle renvoie  _valueiffalse_.
  
## <a name="syntax"></a>Syntaxe

IF(** *logicalexpression* **, ** *valueiftrue* **, ** *valueiffalse* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _logicalexpression_ <br/> |Requis  <br/> |**String** <br/> |Expression à évaluer. |
| _valueiftrue_ <br/> |Requis  <br/> |**Varie** <br/> |Valeur à renvoyer si  _logicalexpression_ est true. |
| _valueiffalse_ <br/> |Requis  <br/> |**Varie** <br/> | Valeur à renvoyer si  _logicalexpression_ est false. |
   
### <a name="return-value"></a>Valeur renvoyée

Variables
  
## <a name="example"></a>Exemple

IF(Height \> 1.25 in,5,7)
  
Renvoie 5 si la hauteur de la forme est supérieure à 31,8 mm. Renvoie 7 si la hauteur de la forme est inférieure ou égale à 31,8 mm.
  

