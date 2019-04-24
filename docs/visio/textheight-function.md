---
title: TEXTHEIGHT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251504
localization_priority: Normal
ms.assetid: 5a10892f-c8fa-c127-2f5a-564009ce5411
description: Renvoie la hauteur du texte composé dans une forme où aucune ligne de texte ne dépasse MaximumWidth.
ms.openlocfilehash: 7455f58f14f9a4a0ae1fcd5375dba5d5860d3852
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332342"
---
# <a name="textheight-function"></a>Fonction TEXTHEIGHT

Renvoie la hauteur du texte composé dans une forme où aucune ligne de texte ne dépasse _MaximumWidth_. 
  
## <a name="syntax"></a>Syntaxe

TEXTHEIGHT (* * *ShapeName! TheText* * * * * *[, MaximumWidth]* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _ShapeName! theText_ <br/> |Obligatoire  <br/> |**String** <br/> |Référence à la cellule nommée TheText dans la forme cible.  _ShapeName!_ est le nom de la forme à partir de laquelle vous souhaitez récupérer le texte.  <br/> |
| _MaximumWidth_ <br/> |Facultatif  <br/> |**Numérique** <br/> |Largeur maximale du bloc de texte.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

La valeur renvoyée comprend la hauteur du texte, ainsi que l’espace précédant et suivant le texte, l’interligne et les marges haut et bas du bloc de texte. Cette fonction est couramment utilisée pour ajuster la hauteur d’une forme au texte qu’elle contient.
  
## <a name="example"></a>Exemple

TEXTHEIGHT(LeTexte,(Largeur - 12,7 mm)) 
  
Renvoie la hauteur du texte développé, lorsque ce dernier est ramené à la largeur de la forme moins 12,7 mm. 
  

