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
description: Indique si la cellule référencée contient une formule locale.
ms.openlocfilehash: 1b749011de8554cb5b777fe92b20a6bcdb2fcb19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788991"
---
# <a name="localformulaexists-function"></a>LOCALFORMULAEXISTS, fonction

Indique si la cellule référencée contient une formule locale. 
  
## <a name="syntax"></a>Syntaxe

LOCALFORMULAEXISTS (** *cellref* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _CellRef_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> | Cellule dans laquelle vous voulez vérifier la présence d’une formule.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Booléenne
  
## <a name="remarks"></a>Remarques

La fonction LOCALFORMULAEXISTS renvoie 1 si la cellule contient une formule locale ; s’il n’y a pas de formule ou si la formule est héritée, elle renvoie 0 (zéro). 
  

