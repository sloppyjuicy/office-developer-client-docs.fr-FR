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
description: Renvoie un nombre binaire de 16 bits dans lequel chaque bit est défini sur 1 uniquement si le bit correspondant en nombre binaire est égal à 0. Dans le cas contraire, le bit prend la valeur 0.
ms.openlocfilehash: 34ea6fd614feae8e3c8e97e34b7ff6c531f4c123
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330008"
---
# <a name="bitnot-function"></a>Fonction BITNOT

Renvoie un nombre binaire de 16 bits dans lequel chaque bit est défini sur 1 uniquement si le bit correspondant en nombre binaire est égal à 0. Dans le cas contraire, le bit prend la valeur 0.
  
## <a name="syntax"></a>Syntaxe

BITNOT (* * *nombre binaire* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _nombre binaire_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Nombre binaire de 16 bits.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Binaire de 16 bits
  
## <a name="example"></a>Exemple

BITNOT (6)
  
Renvoie 65529. Le 6 = 0...00110. Donc, BITNOT(6) = 1...11001.
  

