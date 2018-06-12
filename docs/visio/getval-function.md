---
title: GETVAL, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251885
localization_priority: Normal
ms.assetid: 1da42991-5791-ebab-84cc-286cfe984a61
description: Obtient la valeur d’une cellule et ne recalcule pas la formule lorsque la valeur de cellule est modifiée.
ms.openlocfilehash: b4c8ea14b7184101a360c9f5ee4af03fd178aa6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788718"
---
# <a name="getval-function"></a>GETVAL, fonction

Obtient la valeur d’une cellule et ne recalcule pas la formule lorsque la valeur de cellule est modifiée.
  
## <a name="syntax"></a>Syntaxe

GETVAL (** *cellname* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _cellName_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Nom de la cellule dont la valeur doit être obtenue.  <br/> |
   
## <a name="example"></a>Exemple

GETVAL(PinX) + GETVAL(VY) + Width 
  
Renvoie la somme des valeurs des cellules PinX, PinY et Width. 
  

