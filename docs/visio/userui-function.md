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
ms.openlocfilehash: 6b42860e3e02f1f5e134a29def2eafac7f9b7113
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63378960"
---
# <a name="userui-function"></a>Fonction USERUI

Évalue l’une des deux expressions en fonction de la valeur de  _l’état_.
  
## <a name="syntax"></a>Syntaxe

USERUI(***state** _, _*_defaultexpression_*_, _ *_userexpression_** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _state_ <br/> |Obligatoire  <br/> |**Booléen** <br/> |Détermine l’expression à évaluer. |
| _defaultexpression_ <br/> |Obligatoire  <br/> |**String** <br/> |Expression par défaut. |
| _userexpression_ <br/> |Requis  <br/> |**String** <br/> |Expression fournie par l’utilisateur. |

## <a name="remarks"></a>Remarques

Si  _l’état_ est 0, la fonction USERUI évalue  _l’expression par défaut_. Si  _l’état_ est 1, il évalue  _l’expression utilisateur_.
  
## <a name="example"></a>Exemple

USERUI(1, if(Width6in\>, 6in, Width), Width0.75\*)
  
Évalue l’expression Width.075\* et renvoie le résultat.
  