---
title: GETREF, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251884
ms.localizationpriority: medium
ms.assetid: 25c9f817-d22b-28c9-1339-dc9f27d0dd41
description: Fait référence à une cellule et ne recalcule pas la formule lorsque la cellule référencé change.
ms.openlocfilehash: b2331b18ed78583e745472b02736bd21fb45a104
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628289"
---
# <a name="getref-function"></a>Fonction GETREF

Fait référence à une cellule et ne recalcule pas la formule lorsque la cellule référencé change.
  
## <a name="syntax"></a>Syntaxe

GETREF(** *cellname* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _cellname_ <br/> |Obligatoire  <br/> |**String** <br/> |Nom de la cellule à qui obtenir une référence.  <br/> |
   
## <a name="example"></a>Exemple

SETF(GETREF(PinX),5.1) 
  
Donne à la formule de la cellule PinX la valeur 5,1. 
  

