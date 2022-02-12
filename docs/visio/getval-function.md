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
ms.openlocfilehash: 86588806cca0ea2e36aef0e0085c785e344a454e
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62774257"
---
# <a name="getval-function"></a>Fonction GETVAL

Obtient la valeur d’une cellule et ne recalcule pas la formule lorsque la valeur de la cellule change.
  
## <a name="syntax"></a>Syntaxe

GETVAL(** *cellname* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _cellname_ <br/> |Requis  <br/> |**String** <br/> |Nom de la cellule dont la valeur doit être obtenue. |
   
## <a name="example"></a>Exemple

GETVAL(PinX) + GETVAL(VY) + Width 
  
Renvoie la somme des valeurs des cellules PinX, PinY et Width. 
  

