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
description: Calcule l’une des deux expressions en fonction de la valeur d’état.
ms.openlocfilehash: 2cfdf23986a06dcc109106bd50a1a38e5af91313
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789992"
---
# <a name="userui-function"></a>USERUI, fonction

Calcule l’une des deux expressions en fonction de la valeur _d’état_.
  
## <a name="syntax"></a>Syntaxe

USERUI (** *état* **, ** *expressiondéfaut* **, ** *expressionutil* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _state_ <br/> |Obligatoire  <br/> |**Boolean** <br/> |Détermine l’expression à évaluer.  <br/> |
| _expressiondéfaut_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |L’expression par défaut.  <br/> |
| _expressionutil_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Une expression est fournie par l’utilisateur.  <br/> |
   
## <a name="remarks"></a>Remarques

Si _l’état_ est 0, la fonction USERUI calcule _expressiondéfaut_. Si _l’état_ est 1, elle évalue _expressionutil_.
  
## <a name="example"></a>Exemple

USERUI (1, si (largeur\>en 6, 6 in, largeur), largeur\*0,75) 
  
Évalue l’expression largeur\*.075 et renvoie le résultat. 
  

