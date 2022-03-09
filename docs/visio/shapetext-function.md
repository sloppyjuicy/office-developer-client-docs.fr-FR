---
title: SHAPETEXT, fonction
manager: soliver
ms.date: 03/09/2022
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251788
ms.localizationpriority: medium
ms.assetid: 87ea5e8f-c3e0-009f-4bf8-8c34fbdb83a6
description: Obtient le texte d’une forme.
ms.openlocfilehash: 4e048cfd59c5bc84115f2774fac6ab0115d91782
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63405671"
---
# <a name="shapetext-function"></a>Fonction SHAPETEXT

Obtient le texte d’une forme.
  
## <a name="syntax"></a>Syntaxe

SHAPETEXT (***shapename! TheText** _ _*_[,flag]_** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *shapename! TheText* <br/> |Requis  <br/> ||Référence à la cellule nommée TheText dans la forme cible. *Shapename!* est le nom de la forme à partir de laquelle vous souhaitez récupérer le texte. |
| *flag* <br/> |Facultatif  <br/> |**Numérique** <br/> |Bit qui spécifie le format du texte. L’indicateur par défaut (0) présente le texte exactement tel qu’il apparaît dans la forme. |

### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

Vous pouvez utiliser toute combinaison des indicateurs suivants avec la fonction SHAPETEXT.
  
|**Indicateur**|**Description**|
|:-----|:-----|
|0  <br/> |Présente le texte tel qu’il est affiché dans la forme. |
|1  <br/> |Comprend des tirets. |
|2  <br/> |Ne comprend pas de texte développé dans les champs. |
|4  <br/> |Convertit les tabulations en un espace simple. |
|8   <br/> |Convertit les tabulations en un jeu d’espaces. |
|16  <br/> |Convertit les retours chariot et les sauts de ligne en espaces. |
|32  <br/> |Convertit les guillemets typographiques en guillemets droits. |
|64  <br/> |Convertit plusieurs espaces adjacents en un seul espace. |

## <a name="example-1"></a>Exemple 1

SHAPETEXT(sheetN!theText)
  
Renvoie le texte de la forme nommée feuilleN, exactement tel qu’il apparaît dans la forme.
  
## <a name="example-2"></a>Exemple 2

SHAPETEXT(theText)
  
Renvoie le texte de la forme actuelle exactement tel qu’il apparaît dans la forme.
  
## <a name="example-3"></a>Exemple 3

SHAPETEXT(theText, 84)
  
Renvoie le texte de la forme actuelle. Cet exemple convertit également les espaces adjacents en un seul espace (64), les retours chariot et les sauts de ligne en espaces (16) et les tabulations en un espace simple (4). La somme de ces indicateurs est 84.
  