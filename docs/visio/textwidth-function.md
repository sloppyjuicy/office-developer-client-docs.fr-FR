---
title: TEXTWIDTH, fonction
manager: lindalu
ms.date: 03/09/2022
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251505
ms.localizationpriority: medium
ms.assetid: a9b8efcf-edc0-ad99-deae-21df16c58807
description: Renvoie la largeur du texte composé dans une forme.
ms.openlocfilehash: ef6536b2d316989a221ebeeca0f3726e807b0dca
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63404663"
---
# <a name="textwidth-function"></a>Fonction TEXTWIDTH

Renvoie la largeur du texte composé dans une forme.
  
## <a name="syntax"></a>Syntaxe

TEXTWIDTH(***shapename! TheText** _ _*_[,maximumwidth]_** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *shapename!theText* <br/> |Requis  <br/> |**String** <br/> |Référence à la cellule nommée TheText dans la forme cible.  *shapename!* est le nom de la forme à partir de laquelle vous souhaitez récupérer le texte. |
| *maximumwidth* <br/> |Facultatif  <br/> |**Numérique** <br/> |Largeur maximale du bloc de texte. |

### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

La fonction TEXTWIDTH est couramment utilisée pour ajuster la largeur d’une forme au texte qu’elle contient.
  
If  *sheetN!* est omis, la forme par défaut est la forme actuelle.
  
Si  *la valeur maximumwidth* est spécifiée, le résultat est la ligne de texte la plus longue qui s’adapte _à maximumwidth_. Si _la valeur maximumwidth_ est omise, le résultat est la largeur totale du texte.
  
## <a name="example"></a>Exemple

TEXTWIDTH(TheText)
  
Renvoie la longueur totale du texte dans la forme actuelle.
  