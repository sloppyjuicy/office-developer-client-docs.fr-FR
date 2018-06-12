---
title: BITAND, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251398
localization_priority: Normal
ms.assetid: c437de23-d2e0-469d-62e6-8eb8b8cfea5c
description: Renvoie un nombre binaire de 16 bits dans lequel chaque bit est défini sur 1 uniquement si le bit correspondant dans nombrebinaire1 et nombrebinaire2 est 1. Sinon, le bit est défini sur 0.
ms.openlocfilehash: 0b501bb383596e3f2f39ea14f2cb9eb4bf40b25b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788119"
---
# <a name="bitand-function"></a>BITAND, fonction

Renvoie un nombre binaire de 16 bits dans lequel chaque bit est défini sur 1 uniquement si le bit correspondant dans nombrebinaire1 et nombrebinaire2 est 1. Sinon, le bit est défini sur 0. 
  
## <a name="syntax"></a>Syntaxe

BITAND (** *nombrebinaire1* **, ** *nombrebinaire2* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _nombre1 binaire_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Premier nombre binaire de 16 bits.  <br/> |
| _nombre2 binaire_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Deuxième nombre binaire de 16 bits.  <br/> |
   
## <a name="remarks"></a>Note

Vous pouvez utiliser cette fonction pour tester et modifier les propriétés d’une forme qui sont stockées sous forme de masque de bits, par exemple, le format de texte d’une forme.
  
## <a name="example"></a>Exemple

BITAND(12,6)
  
Renvoie 4. Le 12 = 0...01100. Le 6 = 0...00110. Donc, BITAND(12,6) = 0...00100.
  

