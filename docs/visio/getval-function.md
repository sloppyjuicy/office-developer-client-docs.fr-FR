---
title: GETVAL, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251885
ms.localizationpriority: medium
ms.assetid: 1da42991-5791-ebab-84cc-286cfe984a61
description: Obtient la valeur d’une cellule et ne recalcule pas la formule lorsque la valeur de la cellule change.
ms.openlocfilehash: eb8b138180a0fe40188057c2a35b73421efb9732
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63404529"
---
# <a name="getval-function"></a>Fonction GETVAL

Obtient la valeur d’une cellule et ne recalcule pas la formule lorsque la valeur de la cellule change.
  
## <a name="syntax"></a>Syntaxe

GETVAL(***cellname*** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *cellname* <br/> |Requis  <br/> |**String** <br/> |Nom de la cellule dont la valeur doit être obtenue. |

## <a name="example"></a>Exemple

GETVAL(PinX) + GETVAL(VY) + Width
  
Renvoie la somme des valeurs des cellules PinX, PinY et Width.
  