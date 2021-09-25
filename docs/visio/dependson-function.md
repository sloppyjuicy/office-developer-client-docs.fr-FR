---
title: DEPENDSON, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251420
ms.localizationpriority: medium
ms.assetid: 8fcfcfdd-69e2-b061-fdb6-d29389d14403
description: Crée une dépendance de référence de cellule.
ms.openlocfilehash: f97ba98cbc5e2a56578b5303583a1d2811242f67
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608234"
---
# <a name="dependson-function"></a>Fonction DEPENDSON

Crée une dépendance de référence de cellule.
  
## <a name="syntax"></a>Syntaxe

DEPENDSON(** *cellref* ** [, ** *cellref2* **,...]) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _cellref_ <br/> |Obligatoire  <br/> |**String** <br/> |Première référence de cellule.  <br/> |
| _cellref2_ <br/> |Facultatif  <br/> |**Chaîne** <br/> |Deuxième référence de cellule.  <br/> |
   
## <a name="remarks"></a>Remarques

Cette fonction renvoie toujours la valeur FALSE. Elle n’a pas d’effet lorsqu’elle est utilisée dans une ligne Event ou dans une cellule Action. 
  
## <a name="example"></a>Exemple

OPENTEXTWIN() + DEPENDSON(PinX,PinY) 
  
Ouvre le bloc de texte d’une forme lorsque les cellules PinX ou PinY de la forme sont modifiées. 
  

