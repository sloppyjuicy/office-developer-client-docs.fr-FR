---
title: TEXTWIDTH, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251505
ms.localizationpriority: medium
ms.assetid: a9b8efcf-edc0-ad99-deae-21df16c58807
description: Renvoie la largeur du texte composé dans une forme.
ms.openlocfilehash: 7db00c5d7d0c1e984bb18e786364569afe0ec0e0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627337"
---
# <a name="textwidth-function"></a>Fonction TEXTWIDTH

Renvoie la largeur du texte composé dans une forme. 
  
## <a name="syntax"></a>Syntaxe

TEXTWIDTH(** *shapename! TheText* ** ** *[,maximumwidth]* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _shapename!theText_ <br/> |Obligatoire  <br/> |**String** <br/> |Référence à la cellule nommée TheText dans la forme cible.  _shapename!_ est le nom de la forme à partir de laquelle vous souhaitez récupérer le texte.  <br/> |
| _maximumwidth_ <br/> |Facultatif  <br/> |**Numérique** <br/> |Largeur maximale du bloc de texte.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

La fonction TEXTWIDTH est couramment utilisée pour ajuster la largeur d’une forme au texte qu’elle contient.
  
If  _sheetN!_ est omis, la forme par défaut est la forme actuelle. 
  
Si  _maximumwidth est_ spécifié, le résultat est la ligne de texte la plus longue qui s’adapte  _à maximumwidth_. Si  _la valeur maximumwidth_ est omise, le résultat est la largeur totale du texte. 
  
## <a name="example"></a>Exemple

TEXTWIDTH(TheText) 
  
Renvoie la longueur totale du texte dans la forme actuelle. 
  

