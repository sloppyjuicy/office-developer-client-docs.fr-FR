---
title: ISERROR Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251452
ms.localizationpriority: medium
ms.assetid: 4864ebc2-fee6-2415-7c59-e0af8611f8d6
description: Renvoie TRUE si la valeur de cellreference est un type d’erreur ; Sinon, elle renvoie FALSE. La fonction ISERROR est utilisée dans les formules qui font référence à une autre cellule.
ms.openlocfilehash: 46c339f18b39a8a65762a2201a294df0bc0975bf
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63405064"
---
# <a name="iserror-function-visioshapesheet"></a>ISERROR Function (VisioShapeSheet)

Renvoie TRUE si la valeur de _cellreference_ est un type d’erreur ; Sinon, elle renvoie FALSE. La fonction ISERROR est utilisée dans les formules qui font référence à une autre cellule.
  
## <a name="syntax"></a>Syntaxe

ISERROR(***cellreference*** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _cellreference_ <br/> |Requis  <br/> |**String** <br/> |Référence à une cellule |

## <a name="example-1"></a>Exemple 1

|**Cell**|**Formule**|**Valeur renvoyée**|
|:-----|:-----|:-----|
|Scratch.A1  <br/> |=NA( )  <br/> |#N/A!  <br/> |
|Scratch.B1  <br/> |=ISERROR(Scratch.A1)  <br/> |TRUE  <br/> |

Renvoie TRUE parce que l’erreur #N/A! est reconnue par la fonction ISERROR. Vous pouvez utiliser ISERR pour trouver tous les types d’erreur à l’exception de l’erreur #N/A!.
  
## <a name="example-2"></a>Exemple 2

|**Cell**|**Formule**|**Valeur renvoyée**|
|:-----|:-----|:-----|
|Scratch.X1  <br/> |="House »  <br/> |#VALUE!  <br/> |
|Scratch.B1  <br/> |=ISERROR(Scratch.X1)  <br/> |TRUE  <br/> |

Renvoie TRUE parce que l’erreur #VALEUR! est reconnue par la fonction ISERROR. Pour élaborer une expression basée sur l’erreur #VALEUR!, utilisez la fonction ISERRVALUE.
  