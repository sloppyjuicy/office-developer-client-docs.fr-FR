---
title: SHAPETEXT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251788
localization_priority: Normal
ms.assetid: 87ea5e8f-c3e0-009f-4bf8-8c34fbdb83a6
description: Obtient le texte d'une forme.
ms.openlocfilehash: bb9b1fbe5900cd051828ed6c7ff07546567c1b23
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349111"
---
# <a name="shapetext-function"></a>Fonction SHAPETEXT

Obtient le texte d'une forme. 
  
## <a name="syntax"></a>Syntaxe

SHAPETEXT (* * *ShapeName! TheText* * * * * *[, indicateur]* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _ShapeName! TheText_ <br/> |Obligatoire  <br/> ||Référence à la cellule nommée TheText dans la forme cible.  _ShapeName!_ est le nom de la forme à partir de laquelle vous souhaitez récupérer le texte.  <br/> |
| _flag_ <br/> |Facultatif  <br/> |**Numérique** <br/> |Bit qui spécifie le format du texte. L’indicateur par défaut (0) présente le texte exactement tel qu’il apparaît dans la forme.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

Vous pouvez utiliser toute combinaison des indicateurs suivants avec la fonction SHAPETEXT.
  
|**Indicateur**|**Description**|
|:-----|:-----|
|0  <br/> |Présente le texte tel qu’il est affiché dans la forme.  <br/> |
|0,1  <br/> |Comprend des tirets.  <br/> |
|n°2  <br/> |Ne comprend pas de texte développé dans les champs.  <br/> |
|4  <br/> |Convertit les tabulations en un espace simple.  <br/> |
|8bits  <br/> |Convertit les tabulations en un jeu d’espaces.  <br/> |
|Seiz  <br/> |Convertit les retours chariot et les sauts de ligne en espaces.  <br/> |
|32  <br/> |Convertit les guillemets typographiques en guillemets droits.  <br/> |
|64  <br/> |Convertit plusieurs espaces adjacents en un seul espace.  <br/> |
   
## <a name="example-1"></a>Exemple 1

SHAPETEXT (Sheetn! theText)
  
Renvoie le texte de la forme nommée feuilleN, exactement tel qu’il apparaît dans la forme.
  
## <a name="example-2"></a>Exemple 2

SHAPETEXT (theText)
  
Renvoie le texte de la forme actuelle exactement tel qu’il apparaît dans la forme.
  
## <a name="example-3"></a>Exemple 3

SHAPETEXT(theText, 84)
  
Renvoie le texte de la forme actuelle. Cet exemple convertit également les espaces adjacents en un seul espace (64), les retours chariot et les sauts de ligne en espaces (16) et les tabulations en un espace simple (4). La somme de ces indicateurs est 84.
  

