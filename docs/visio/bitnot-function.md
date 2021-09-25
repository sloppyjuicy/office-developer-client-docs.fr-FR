---
title: BITNOT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251399
ms.localizationpriority: medium
ms.assetid: 7b6486bb-3618-3747-4b00-93bd55767c1c
description: Renvoie un nombre binaire 16 bits dans lequel chaque bit est définie sur 1 uniquement si le bit correspondant dans le nombre binaire est 0. Dans le cas contraire, le bit est définie sur 0.
ms.openlocfilehash: 66a394ea9627d72e927c0b0cf4a001b4a1994dda
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554872"
---
# <a name="bitnot-function"></a>Fonction BITNOT

Renvoie un nombre binaire 16 bits dans lequel chaque bit est définie sur 1 uniquement si le bit correspondant dans le nombre binaire est 0. Dans le cas contraire, le bit est définie sur 0.
  
## <a name="syntax"></a>Syntaxe

BITNOT(** *binary number* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _nombre binaire_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Nombre binaire de 16 bits.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Binaire de 16 bits
  
## <a name="example"></a>Exemple

BITNOT(6)
  
Renvoie 65529. Le 6 = 0...00110. Donc, BITNOT(6) = 1...11001.
  

