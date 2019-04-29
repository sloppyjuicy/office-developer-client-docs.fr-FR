---
title: MAGNITUDE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251461
localization_priority: Normal
ms.assetid: 9f443687-9861-5f51-94c4-f056805f736b
description: Renvoie l'amplitude du vecteur dont la hauteur est A et dont l'exécution est B, multipliée par les constantes constanteA et constanteB.
ms.openlocfilehash: 6393c7827e2553ca4948c8b9c51075ca8e4783bd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420457"
---
# <a name="magnitude-function"></a>Fonction MAGNITUDE

Renvoie l'amplitude du vecteur dont la hauteur est _a_ et dont l'exécution est _B_, multipliée par les constantes _constanteA_ et _constanteB_. 
  
## <a name="syntax"></a>Syntaxe

AMPLITUDE (* * *constanteA* * *, * * *A* * *, * * *constanteB* * *, * * *B* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _constanteA_ <br/> |Obligatoire  <br/> |**Number** <br/> |Constante par laquelle multiplier la hauteur  <br/> |
| _A_ <br/> |Obligatoire  <br/> |**Number** <br/> |Hauteur  <br/> |
| _constanteB_ <br/> |Obligatoire  <br/> |**Number** <br/> |Constante par laquelle multiplier la longueur  <br/> |
| _Point_ <br/> |Obligatoire  <br/> |**Number** <br/> |Longueur  <br/> |
   
## <a name="remarks"></a>Remarques

La fonction MAGNITUDE est calculée selon la formule suivante :
  
SQRT ((constanteA \* A) ^ 2 + (constanteB \* B) ^ 2)
  
## <a name="example"></a>Exemple

MAGNITUDE(1; 3; 1; 4) 
  
Renvoie 5. 
  

