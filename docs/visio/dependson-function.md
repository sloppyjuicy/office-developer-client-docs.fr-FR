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
ms.openlocfilehash: 36366b51e6eedb0bcf8d3af89368f34977f8aa4c
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62771642"
---
# <a name="dependson-function"></a>Fonction DEPENDSON

Crée une dépendance de référence de cellule.
  
## <a name="syntax"></a>Syntaxe

DEPENDSON(** *cellref* ** [, ** *cellref2* **,...]) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _cellref_ <br/> |Requis  <br/> |**String** <br/> |Première référence de cellule. |
| _cellref2_ <br/> |Facultatif  <br/> |**Chaîne** <br/> |Deuxième référence de cellule. |
   
## <a name="remarks"></a>Remarques

Cette fonction renvoie toujours la valeur FALSE. Elle n’a pas d’effet lorsqu’elle est utilisée dans une ligne Event ou dans une cellule Action. 
  
## <a name="example"></a>Exemple

OPENTEXTWIN() + DEPENDSON(PinX,PinY) 
  
Ouvre le bloc de texte d’une forme lorsque les cellules PinX ou PinY de la forme sont modifiées. 
  

