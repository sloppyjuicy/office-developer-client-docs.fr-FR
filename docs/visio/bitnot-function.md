---
title: BITNOT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251399
localization_priority: Normal
ms.assetid: 7b6486bb-3618-3747-4b00-93bd55767c1c
description: Renvoie un nombre binaire de 16 bits dans lequel chaque bit est défini sur 1 uniquement si le bit correspondant dans nombre binaire est égal à 0. Sinon, le bit est défini sur 0.
ms.openlocfilehash: 0806e7c52cab659a09d27a60efb9c09aa436fb92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788094"
---
# <a name="bitnot-function"></a>BITNOT, fonction

Renvoie un nombre binaire de 16 bits dans lequel chaque bit est défini sur 1 uniquement si le bit correspondant dans nombre binaire est égal à 0. Sinon, le bit est défini sur 0.
  
## <a name="syntax"></a>Syntaxe

BITNOT (** *nombre binaire* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _nombre binaire_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Nombre binaire de 16 bits.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Binaire de 16 bits
  
## <a name="example"></a>Exemple

BITNOT(6)
  
Renvoie 65529. Le 6 = 0...00110. Donc, BITNOT(6) = 1...11001.
  

