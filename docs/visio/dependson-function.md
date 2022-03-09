---
title: DEPENDSON, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251420
ms.localizationpriority: medium
ms.assetid: 8fcfcfdd-69e2-b061-fdb6-d29389d14403
description: Crée une dépendance de référence de cellule.
ms.openlocfilehash: 95668a38f81abd8a5e45cd00756f7e83da115e9e
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63404501"
---
# <a name="dependson-function"></a>Fonction DEPENDSON

Crée une dépendance de référence de cellule.
  
## <a name="syntax"></a>Syntaxe

DEPENDSON(***cellref** _ [, _*_cellref2_**,...])
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *cellref* <br/> |Requis  <br/> |**String** <br/> |Première référence de cellule. |
| *cellref2* <br/> |Facultatif  <br/> |**Chaîne** <br/> |Deuxième référence de cellule. |

## <a name="remarks"></a>Remarques

Cette fonction renvoie toujours la valeur FALSE. Elle n’a pas d’effet lorsqu’elle est utilisée dans une ligne Event ou dans une cellule Action.
  
## <a name="example"></a>Exemple

OPENTEXTWIN() + DEPENDSON(PinX,PinY)
  
Ouvre le bloc de texte d’une forme lorsque les cellules PinX ou PinY de la forme sont modifiées.
  