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
description: Renvoie la hauteur du texte composé dans une forme où aucune ligne de texte ne dépasse le maximumwidth.
ms.openlocfilehash: 7455f58f14f9a4a0ae1fcd5375dba5d5860d3852
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427408"
---
# <a name="textheight-function"></a>Fonction TEXTHEIGHT

Renvoie la hauteur du texte composé dans une forme où aucune ligne de texte ne dépasse  _maximumwidth_. 
  
## <a name="syntax"></a>Syntaxe

TEXTHEIGHT(** *shapename! TheText* ** ** *[,maximumwidth]* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _shapename!theText_ <br/> |Obligatoire  <br/> |**String** <br/> |Référence à la cellule nommée TheText dans la forme cible.  _shapename!_ est le nom de la forme à partir de laquelle vous souhaitez récupérer le texte.  <br/> |
| _maximumwidth_ <br/> |Facultatif  <br/> |**Numérique** <br/> |Largeur maximale du bloc de texte.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

La valeur renvoyée comprend la hauteur du texte, ainsi que l’espace précédant et suivant le texte, l’interligne et les marges haut et bas du bloc de texte. Cette fonction est couramment utilisée pour ajuster la hauteur d’une forme au texte qu’elle contient.
  
## <a name="example"></a>Exemple

TEXTHEIGHT(LeTexte,(Largeur - 12,7 mm)) 
  
Renvoie la hauteur du texte développé, lorsque ce dernier est ramené à la largeur de la forme moins 12,7 mm. 
  

