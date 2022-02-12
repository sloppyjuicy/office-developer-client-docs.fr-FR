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
ms.openlocfilehash: 484752d427a88744f7d29ef624c229a3f4c5c3ce
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62774250"
---
# <a name="getref-function"></a>Fonction GETREF

Fait référence à une cellule et ne recalcule pas la formule lorsque la cellule référencé change.
  
## <a name="syntax"></a>Syntaxe

GETREF(** *cellname* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _cellname_ <br/> |Requis  <br/> |**String** <br/> |Nom de la cellule à qui obtenir une référence. |
   
## <a name="example"></a>Exemple

SETF(GETREF(PinX),5.1) 
  
Donne à la formule de la cellule PinX la valeur 5,1. 
  

