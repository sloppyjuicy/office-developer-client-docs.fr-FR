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
description: Renvoie la hauteur du texte composé dans une forme où aucune ligne ne dépasse la valeur largeurmaximale.
ms.openlocfilehash: 9a80dafcf80a1dcba968a0f60465aae4e2a2758b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789875"
---
# <a name="textheight-function"></a>TEXTHEIGHT, fonction

Renvoie la hauteur du texte composé dans une forme où aucune ligne ne dépasse la _valeur largeurmaximale_. 
  
## <a name="syntax"></a>Syntaxe

TEXTHEIGHT (** shapename *! TheText* ** ** *[, largeurmaximale]* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _l’argument shapename ! theText_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Une référence à la cellule nommée TheText dans la forme cible.  _argument shapename !_ est le nom de la forme à partir de laquelle vous souhaitez récupérer le texte.  <br/> |
| _largeurmaximale_ <br/> |Facultatif  <br/> |**Numérique** <br/> |Largeur maximale du bloc de texte.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Chaîne
  
## <a name="remarks"></a>Remarques

La valeur renvoyée comprend la hauteur du texte, ainsi que l’espace précédant et suivant le texte, l’interligne et les marges haut et bas du bloc de texte. Cette fonction est couramment utilisée pour ajuster la hauteur d’une forme au texte qu’elle contient.
  
## <a name="example"></a>Exemple

TEXTHEIGHT(LeTexte,(Largeur - 12,7 mm)) 
  
Renvoie la hauteur du texte développé, lorsque ce dernier est ramené à la largeur de la forme moins 12,7 mm. 
  

