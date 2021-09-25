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
ms.openlocfilehash: fe5af032eae84612963913a23f94e65708e5ec8c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582665"
---
# <a name="getval-function"></a>Fonction GETVAL

Obtient la valeur d’une cellule et ne recalcule pas la formule lorsque la valeur de la cellule change.
  
## <a name="syntax"></a>Syntaxe

GETVAL(** *cellname* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _cellname_ <br/> |Obligatoire  <br/> |**String** <br/> |Nom de la cellule dont la valeur doit être obtenue.  <br/> |
   
## <a name="example"></a>Exemple

GETVAL(PinX) + GETVAL(VY) + Width 
  
Renvoie la somme des valeurs des cellules PinX, PinY et Width. 
  

