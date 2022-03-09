---
title: ISERRNA, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251451
ms.localizationpriority: medium
ms.assetid: 6ee7dc3d-efe9-c862-f71d-034b3d9c3ec6
description: 'Renvoie TRUE si la valeur de cellreference est de type erreur #N/A! (non disponible) ; Sinon, elle renvoie FALSE. La fonction ISERRNA est utilisée dans les formules qui font référence à une autre cellule.'
ms.openlocfilehash: 459b183258d4921a6c5e6577a9de34f100cd983f
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63406102"
---
# <a name="iserrna-function"></a>Fonction ISERRNA

Renvoie TRUE si la valeur de _cellreference_ est de type erreur #N/A! (non disponible) ; Sinon, elle renvoie FALSE. La fonction ISERRNA est utilisée dans les formules qui font référence à une autre cellule.
  
## <a name="syntax"></a>Syntaxe

ISERRNA(***cellreference*** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _cellreference_ <br/> |Requis  <br/> |**String** <br/> |Référence à une cellule |

## <a name="example-1"></a>Exemple 1

|**Cell**|**Formule**|**Valeur renvoyée**|
|:-----|:-----|:-----|
|Scratch.A1  <br/> |="5 + 3"  <br/> |"8"  <br/> |
|Scratch.B1  <br/> |=ISERRNA(Scratch.A1)  <br/> |FALSE  <br/> |

Renvoie FALSE parce que la valeur renvoyée est disponible.
  
## <a name="example-2"></a>Exemple 2

|**Cell**|**Formule**|**Valeur renvoyée**|
|:-----|:-----|:-----|
|Scratch.A1  <br/> |=NA( )  <br/> |#N/A!  <br/> |
|Scratch.B1  <br/> |=ISERRNA(Scratch.A1)  <br/> |TRUE  <br/> |

Renvoie TRUE parce que la valeur renvoyée est du type d’erreur #N/A!
  