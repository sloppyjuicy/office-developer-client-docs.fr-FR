---
title: GETREF, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251884
localization_priority: Normal
ms.assetid: 25c9f817-d22b-28c9-1339-dc9f27d0dd41
description: Fait référence à une cellule et ne recalcule pas la formule lorsque la cellule référencée change.
ms.openlocfilehash: 454314b1f156f560c237f22a45492978ca3c31ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788716"
---
# <a name="getref-function"></a>GETREF, fonction

Fait référence à une cellule et ne recalcule pas la formule lorsque la cellule référencée change.
  
## <a name="syntax"></a>Syntaxe

GETREF (** *cellname* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _cellName_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Le nom de la cellule pour obtenir une référence à.  <br/> |
   
## <a name="example"></a>Exemple

SETF(GETREF(PinX),5.1) 
  
Donne à la formule de la cellule PinX la valeur 5,1. 
  

