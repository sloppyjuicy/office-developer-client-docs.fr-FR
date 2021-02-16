---
title: IF, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251442
localization_priority: Normal
ms.assetid: 66771ad3-0fb3-68ff-81da-d1162d37c05a
description: Renvoie valueiftrue si logicalexpression a la valeur TRUE. Sinon, elle renvoie valueiffalse.
ms.openlocfilehash: 8780bd3dd5ded1a950a5bf3f79333687f3b6843c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405470"
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
  

