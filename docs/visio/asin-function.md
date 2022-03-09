---
title: ASIN, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251395
ms.localizationpriority: medium
ms.assetid: 7d917be4-65b1-002f-48cc-6d81916a1157
description: Renvoie l’arc sinus d’un nombre (par exemple, l’angle dont le sinus a la valeur nombre).
ms.openlocfilehash: ec77daeddf88d9ad5e5a4acfbe6e828ef2067593
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63380360"
---
# <a name="asin-function"></a>Fonction ASIN

Renvoie l’arc sinus d’un nombre (par exemple, l’angle dont le sinus a la valeur *nombre*).
  
## <a name="syntax"></a>Syntaxe

ASIN(***number*** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *number* <br/> |Obligatoire  <br/> |**Numérique** <br/> |Sinus de l’angle. |

## <a name="remarks"></a>Remarques

La valeur d’entrée doit être dans la plage -1 <=  *nombre*  <= 1 ou une valeur #NUM! est renvoyée. L’angle obtenu se situe dans la limite -PI/2 <= *angle* <= PI/2 radians (soit -90 <= *angle* <= 90 degrés).
  
## <a name="example"></a>Exemple

ASIN(1)
  
Renvoie 90 deg
  