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
ms.openlocfilehash: a7a1aa25eb96c6e81632420a3ac69b24ab27364d
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62772485"
---
# <a name="textwidth-function"></a>Fonction TEXTWIDTH

Renvoie la largeur du texte composé dans une forme. 
  
## <a name="syntax"></a>Syntaxe

TEXTWIDTH(** *shapename! TheText* ** ** *[,maximumwidth]* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _shapename!theText_ <br/> |Requis  <br/> |**String** <br/> |Référence à la cellule nommée TheText dans la forme cible.  _shapename!_ est le nom de la forme à partir de laquelle vous souhaitez récupérer le texte. |
| _maximumwidth_ <br/> |Facultatif  <br/> |**Numérique** <br/> |Largeur maximale du bloc de texte. |
   
### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

La fonction TEXTWIDTH est couramment utilisée pour ajuster la largeur d’une forme au texte qu’elle contient.
  
If  _sheetN!_ est omis, la forme par défaut est la forme actuelle. 
  
Si  _la valeur maximumwidth_ est spécifiée, le résultat est la ligne de texte la plus longue qui s’adapte  _à maximumwidth_. Si  _la valeur maximumwidth_ est omise, le résultat est la largeur totale du texte. 
  
## <a name="example"></a>Exemple

TEXTWIDTH(TheText) 
  
Renvoie la longueur totale du texte dans la forme actuelle. 
  

