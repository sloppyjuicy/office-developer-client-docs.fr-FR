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
ms.openlocfilehash: d9eab4f1f1060a9d1390f474486856f031897e84
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63404621"
---
# <a name="localformulaexists-function"></a>Fonction LOCALFORMULAEXISTS

Indique si la cellule référencé contient une formule locale.
  
## <a name="syntax"></a>Syntaxe

LOCALFORMULAEXISTS (***cellref*** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *cellref* <br/> |Requis  <br/> |**String** <br/> | Cellule dans laquelle vous voulez vérifier la présence d’une formule. |

### <a name="return-value"></a>Valeur renvoyée

Booléen
  
## <a name="remarks"></a>Remarques

La fonction LOCALFORMULAEXISTS renvoie 1 si la cellule contient une formule locale ; s’il n’y a pas de formule ou si la formule est héritée, elle renvoie 0 (zéro).
  