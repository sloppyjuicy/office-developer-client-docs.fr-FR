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
ms.openlocfilehash: 2fdd6e547f1f86491fc84d316237d472e767536b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603654"
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
  

