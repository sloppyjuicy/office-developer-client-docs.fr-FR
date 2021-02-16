---
title: USERUI, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251511
localization_priority: Normal
ms.assetid: c01dd938-677c-b2ba-8f56-4638e7e988fd
description: Évalue l’une des deux expressions en fonction de la valeur de l’état.
ms.openlocfilehash: 544bb2b19dc610591afc78c407301098fac9c7c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420345"
---
# <a name="userui-function"></a>Fonction USERUI

Évalue l’une des deux expressions en fonction de la valeur de  _l’état_.
  
## <a name="syntax"></a>Syntaxe

USERUI(** *state* **, ** *defaultexpression* **, ** *userexpression* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _state_ <br/> |Obligatoire  <br/> |**Booléen** <br/> |Détermine l’expression à évaluer.  <br/> |
| _defaultexpression_ <br/> |Obligatoire  <br/> |**String** <br/> |Expression par défaut.  <br/> |
| _userexpression_ <br/> |Obligatoire  <br/> |**String** <br/> |Expression fournie par l’utilisateur.  <br/> |
   
## <a name="remarks"></a>Remarques

Si _l’état_ est 0, la fonction USERUI évalue _l’expression par défaut._ Si  _l’état_ est 1, il évalue  _l’expression utilisateur_.
  
## <a name="example"></a>Exemple

USERUI(1, if(Width \> 6in, 6in, Width), Width \* 0.75) 
  
Évalue l’expression Width \* .075 et renvoie le résultat. 
  

