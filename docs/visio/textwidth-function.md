---
title: TEXTWIDTH, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251505
localization_priority: Normal
ms.assetid: a9b8efcf-edc0-ad99-deae-21df16c58807
description: Renvoie la largeur du texte composé dans une forme.
ms.openlocfilehash: 43848bba4d24a0c31a3a084d123cd56140bf0709
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332269"
---
# <a name="textwidth-function"></a>Fonction TEXTWIDTH

Renvoie la largeur du texte composé dans une forme. 
  
## <a name="syntax"></a>Syntaxe

TEXTWIDTH (* * *ShapeName! TheText* * * * * *[, MaximumWidth]* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _ShapeName! theText_ <br/> |Obligatoire  <br/> |**String** <br/> |Référence à la cellule nommée TheText dans la forme cible.  _ShapeName!_ est le nom de la forme à partir de laquelle vous souhaitez récupérer le texte.  <br/> |
| _MaximumWidth_ <br/> |Facultatif  <br/> |**Numérique** <br/> |Largeur maximale du bloc de texte.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

La fonction TEXTWIDTH est couramment utilisée pour ajuster la largeur d’une forme au texte qu’elle contient.
  
Si _Sheetn!_ est omis, la forme par défaut est la forme active. 
  
Si _MaximumWidth_ est spécifié, le résultat est la plus longue ligne de texte qui correspond à _MaximumWidth_. Si _MaximumWidth_ est omis, le résultat est la largeur totale du texte. 
  
## <a name="example"></a>Exemple

TEXTWIDTH (TheText) 
  
Renvoie la longueur totale du texte de la forme active. 
  

