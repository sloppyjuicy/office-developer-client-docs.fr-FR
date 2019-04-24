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
description: Évalue l'une des deux expressions en fonction de la valeur de State.
ms.openlocfilehash: 544bb2b19dc610591afc78c407301098fac9c7c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331324"
---
# <a name="userui-function"></a>Fonction USERUI

Évalue l'une des deux expressions en fonction de la valeur de _State_.
  
## <a name="syntax"></a>Syntaxe

USERUI (* * *État* * *, * * *DefaultExpression* * *, * * *userexpression* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _state_ <br/> |Obligatoire  <br/> |**Booléen** <br/> |Détermine l'expression à évaluer.  <br/> |
| _DefaultExpression_ <br/> |Obligatoire  <br/> |**String** <br/> |Expression par défaut.  <br/> |
| _userexpression_ <br/> |Obligatoire  <br/> |**String** <br/> |Expression fournie par l'utilisateur.  <br/> |
   
## <a name="remarks"></a>Remarques

Si _State_ est égal à 0, la fonction USERUI évalue la _DefaultExpression_. Si _State_ est égal à 1, il évalue le _userexpression_.
  
## <a name="example"></a>Exemple

USERUI (1, si (largeur\>6in, 6In, largeur), largeur\*0,75) 
  
Évalue la largeur\*de l'expression 075 et renvoie le résultat. 
  

