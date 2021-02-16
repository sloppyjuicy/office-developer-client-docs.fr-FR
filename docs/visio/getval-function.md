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
description: Obtient la valeur d’une cellule et ne recalcule pas la formule lorsque la valeur de la cellule change.
ms.openlocfilehash: 9449ccd8f849b23faf08ee25826301a1b6efe6d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416887"
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
  

