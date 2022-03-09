---
title: TEXTHEIGHT, fonction
manager: lindalu
ms.date: 03/09/2022
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251504
ms.localizationpriority: medium
ms.assetid: 5a10892f-c8fa-c127-2f5a-564009ce5411
description: Renvoie la hauteur du texte composé dans une forme où aucune ligne de texte ne dépasse le maximumwidth.
ms.openlocfilehash: 48523028161e774b3a2771cde04d3c2ee5873b9f
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63405899"
---
# <a name="textheight-function"></a>Fonction TEXTHEIGHT

Renvoie la hauteur du texte composé dans une forme où aucune ligne de texte ne dépasse _le maximumwidth_.
  
## <a name="syntax"></a>Syntaxe

TEXTHEIGHT(***shapename! TheText** _ _*_[,maximumwidth]_**)
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _shapename!theText_ <br/> |Requis  <br/> |**String** <br/> |Référence à la cellule nommée TheText dans la forme cible. _shapename!_ est le nom de la forme à partir de laquelle vous souhaitez récupérer le texte. |
| _maximumwidth_ <br/> |Facultatif  <br/> |**Numérique** <br/> |Largeur maximale du bloc de texte. |

### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

La valeur renvoyée comprend la hauteur du texte, ainsi que l’espace précédant et suivant le texte, l’interligne et les marges haut et bas du bloc de texte. Cette fonction est couramment utilisée pour ajuster la hauteur d’une forme au texte qu’elle contient.
  
## <a name="example"></a>Exemple

TEXTHEIGHT(LeTexte,(Largeur - 12,7 mm))
  
Renvoie la hauteur du texte développé, lorsque ce dernier est ramené à la largeur de la forme moins 12,7 mm.
  