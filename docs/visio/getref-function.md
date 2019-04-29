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
ms.openlocfilehash: 38f3c8b4f34ed2b3d3711be5faed6b0d317e907a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424328"
---
# <a name="getref-function"></a>Fonction GETREF

Fait référence à une cellule et ne recalcule pas la formule lorsque la cellule référencée change.
  
## <a name="syntax"></a>Syntaxe

GETREF (* * *cellName* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _cellName_ <br/> |Obligatoire  <br/> |**String** <br/> |Nom de la cellule pour laquelle obtenir une référence.  <br/> |
   
## <a name="example"></a>Exemple

SETF (GETREF (PinX), 5.1) 
  
Donne à la formule de la cellule PinX la valeur 5,1. 
  

