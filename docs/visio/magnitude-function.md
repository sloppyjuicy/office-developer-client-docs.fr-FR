---
title: MAGNITUDE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251461
ms.localizationpriority: medium
ms.assetid: 9f443687-9861-5f51-94c4-f056805f736b
description: Renvoie la magnitude du vecteur dont la montée est A et dont la run est B, multipliée par les constantes respectives constantA et constantB.
ms.openlocfilehash: ac3eb76ad2ad5c20e76f391c6ceedea50d1c3d8d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582504"
---
# <a name="magnitude-function"></a>Fonction MAGNITUDE

Renvoie la magnitude du vecteur dont la montée est  _A_ et dont la run est  _B_, multipliée par les constantes respectives  _constantA_ et  _constantB_. 
  
## <a name="syntax"></a>Syntaxe

MAGNITUDE(** *constantA* **, ** *A* **, ** *constantB* **, ** *B* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _constantA_ <br/> |Obligatoire  <br/> |**Number** <br/> |Constante par laquelle multiplier la hauteur  <br/> |
| _A_ <br/> |Obligatoire  <br/> |**Number** <br/> |Hauteur  <br/> |
| _constantB_ <br/> |Obligatoire  <br/> |**Number** <br/> |Constante par laquelle multiplier la longueur  <br/> |
| _B_ <br/> |Obligatoire  <br/> |**Number** <br/> |Longueur  <br/> |
   
## <a name="remarks"></a>Remarques

La fonction MAGNITUDE est calculée selon la formule suivante :
  
SQRT((constantA \* A)^2 + (constantB \* B)^2)
  
## <a name="example"></a>Exemple

MAGNITUDE(1; 3; 1; 4) 
  
Renvoie 5. 
  

