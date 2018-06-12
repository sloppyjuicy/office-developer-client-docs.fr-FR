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
description: Obtient le texte d’une forme.
ms.openlocfilehash: 53a0cb6e485ae2fd233792e1ebd9765426b7f798
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789685"
---
# <a name="shapetext-function"></a>SHAPETEXT, fonction

Obtient le texte d’une forme. 
  
## <a name="syntax"></a>Syntaxe

SHAPETEXT (** shapename *! TheText* ** ** *[, indicateur]* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _argument shapename ! TheText_ <br/> |Obligatoire  <br/> ||Une référence à la cellule nommée TheText dans la forme cible.  _Argument shapename !_ est le nom de la forme à partir de laquelle vous souhaitez récupérer le texte.  <br/> |
| _indicateur_ <br/> |Facultatif  <br/> |**Numérique** <br/> |Bit qui spécifie le format du texte. L’indicateur par défaut (0) présente le texte exactement tel qu’il apparaît dans la forme.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Chaîne
  
## <a name="remarks"></a>Remarques

Vous pouvez utiliser toute combinaison des indicateurs suivants avec la fonction SHAPETEXT.
  
|**Indicateur**|**Description**|
|:-----|:-----|
|0  <br/> |Présente le texte tel qu’il est affiché dans la forme.  <br/> |
|1  <br/> |Comprend des tirets.  <br/> |
|2  <br/> |Ne comprend pas de texte développé dans les champs.  <br/> |
|4  <br/> |Convertit les tabulations en un espace simple.  <br/> |
|8  <br/> |Convertit les tabulations en un jeu d’espaces.  <br/> |
|16  <br/> |Convertit les retours chariot et les sauts de ligne en espaces.  <br/> |
|32  <br/> |Convertit les guillemets typographiques en guillemets droits.  <br/> |
|64  <br/> |Convertit plusieurs espaces adjacents en un seul espace.  <br/> |
   
## <a name="example-1"></a>Exemple 1

SHAPETEXT(sheetN!TheText)
  
Renvoie le texte de la forme nommée feuilleN, exactement tel qu’il apparaît dans la forme.
  
## <a name="example-2"></a>Exemple 2

SHAPETEXT(TheText)
  
Renvoie le texte de la forme actuelle exactement tel qu’il apparaît dans la forme.
  
## <a name="example-3"></a>Exemple 3

SHAPETEXT(theText, 84)
  
Renvoie le texte de la forme actuelle. Cet exemple convertit également les espaces adjacents en un seul espace (64), les retours chariot et les sauts de ligne en espaces (16) et les tabulations en un espace simple (4). La somme de ces indicateurs est 84.
  

