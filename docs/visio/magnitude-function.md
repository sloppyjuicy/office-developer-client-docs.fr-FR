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
description: Renvoie l’ampleur du vecteur dont la hauteur est A et dont est B, multiplié par respectifs constantes constanteA et constanteB.
ms.openlocfilehash: f4c428b8b381af58958dab66a71ddd0bcaf715c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789058"
---
# <a name="magnitude-function"></a>MAGNITUDE, fonction

Renvoie l’ampleur du vecteur dont la hauteur est _A_ et dont est _B_multipliée par les constantes respectives _constanteA_ et _constanteB_. 
  
## <a name="syntax"></a>Syntaxe

MAGNITUDE (** *constanteA* **, ** *A* **, ** *constanteB* **, ** *B* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _constanteA_ <br/> |Obligatoire  <br/> |**Number** <br/> |Constante par laquelle multiplier la hauteur  <br/> |
| _A_ <br/> |Obligatoire  <br/> |**Number** <br/> |Hauteur  <br/> |
| _constanteB_ <br/> |Obligatoire  <br/> |**Number** <br/> |Constante par laquelle multiplier la longueur  <br/> |
| _B_ <br/> |Obligatoire  <br/> |**Number** <br/> |Longueur  <br/> |
   
## <a name="remarks"></a>Note

La fonction MAGNITUDE est calculée selon la formule suivante :
  
SQRT ((constanteA \* A) ^ 2 + (constanteB \* B) ^ 2)
  
## <a name="example"></a>Exemple

MAGNITUDE(1; 3; 1; 4) 
  
Renvoie 5. 
  

