---
title: LOCALFORMULAEXISTS, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60105
ms.localizationpriority: medium
ms.assetid: 2b757c8d-7732-0f9b-c836-ef755dd1c673
description: Indique si la cellule référencé contient une formule locale.
ms.openlocfilehash: b9098dbe9b30e6ce6390c8b20347419449f73708
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62780651"
---
# <a name="localformulaexists-function"></a>Fonction LOCALFORMULAEXISTS

Indique si la cellule référencé contient une formule locale. 
  
## <a name="syntax"></a>Syntaxe

LOCALFORMULAEXISTS (** *cellref* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _cellref_ <br/> |Requis  <br/> |**String** <br/> | Cellule dans laquelle vous voulez vérifier la présence d’une formule. |
   
### <a name="return-value"></a>Valeur renvoyée

Booléen
  
## <a name="remarks"></a>Remarques

La fonction LOCALFORMULAEXISTS renvoie 1 si la cellule contient une formule locale ; s’il n’y a pas de formule ou si la formule est héritée, elle renvoie 0 (zéro). 
  

