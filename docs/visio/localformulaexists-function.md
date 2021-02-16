---
title: LOCALFORMULAEXISTS, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60105
localization_priority: Normal
ms.assetid: 2b757c8d-7732-0f9b-c836-ef755dd1c673
description: Indique si la cellule référencé contient une formule locale.
ms.openlocfilehash: bd0a5dafecf1bd8dca1567392d880ecaaa3e0374
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433289"
---
# <a name="localformulaexists-function"></a>Fonction LOCALFORMULAEXISTS

Indique si la cellule référencé contient une formule locale. 
  
## <a name="syntax"></a>Syntaxe

LOCALFORMULAEXISTS (** *cellref* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _cellref_ <br/> |Obligatoire  <br/> |**String** <br/> | Cellule dans laquelle vous voulez vérifier la présence d’une formule.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Booléen
  
## <a name="remarks"></a>Remarques

La fonction LOCALFORMULAEXISTS renvoie 1 si la cellule contient une formule locale ; s’il n’y a pas de formule ou si la formule est héritée, elle renvoie 0 (zéro). 
  

