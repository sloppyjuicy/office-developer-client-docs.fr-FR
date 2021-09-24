---
title: USERUI, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251511
ms.localizationpriority: medium
ms.assetid: c01dd938-677c-b2ba-8f56-4638e7e988fd
description: Évalue l’une des deux expressions en fonction de la valeur de l’état.
ms.openlocfilehash: 8e26154b6d6f4f8102380d03ee95417a09994567
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549356"
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
  

