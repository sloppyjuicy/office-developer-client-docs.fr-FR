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
ms.openlocfilehash: d96b9489c08ce38205f8e9ad91e361fcb643c39c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789873"
---
# <a name="textwidth-function"></a>TEXTWIDTH, fonction

Renvoie la largeur du texte composé dans une forme. 
  
## <a name="syntax"></a>Syntaxe

TEXTWIDTH (** shapename *! TheText* ** ** *[, largeurmaximale]* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _l’argument shapename ! theText_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Une référence à la cellule nommée TheText dans la forme cible.  _argument shapename !_ est le nom de la forme à partir de laquelle vous souhaitez récupérer le texte.  <br/> |
| _largeurmaximale_ <br/> |Facultatif  <br/> |**Numérique** <br/> |Largeur maximale du bloc de texte.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Chaîne
  
## <a name="remarks"></a>Remarques

La fonction TEXTWIDTH est couramment utilisée pour ajuster la largeur d’une forme au texte qu’elle contient.
  
Si _feuilleN !_ est omis, la forme par défaut est la forme active. 
  
Si la _valeur largeurmaximale_ est indiquée, le résultat est la plus longue ligne de texte dans la _largeurmaximale_. Si la _valeur largeurmaximale_ est omise, le résultat est la largeur totale du texte. 
  
## <a name="example"></a>Exemple

TextWidth(TheText) 
  
Renvoie la longueur totale du texte figurant dans la forme active. 
  

