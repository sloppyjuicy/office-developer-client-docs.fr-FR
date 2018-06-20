---
title: BITOR, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251400
localization_priority: Normal
ms.assetid: 1d0954c5-b2cb-6c5d-62b3-a68011cf0c85
description: Renvoie un nombre binaire de 16 bits dans lequel chaque bit a la valeur 1 si le bit correspondant dans Numéro1 binaire ou binaire nombre2 est 1. Le bit est défini sur 0 uniquement si le bit correspondant est 0 en binaire Numéro1 et numéro2 binaire.
ms.openlocfilehash: db9808f16b32776149abbddf882310c02268cec3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788111"
---
# <a name="bitor-function"></a>BITOR, fonction

Renvoie un nombre binaire de 16 bits dans lequel chaque bit a la valeur 1 si le bit correspondant dans *Numéro1 binaire* ou *binaire nombre2* est 1. Le bit est défini sur 0 uniquement si le bit correspondant est 0 en *binaire Numéro1* et *Numéro2 binaire* . 
  
## <a name="syntax"></a>Syntaxe

BITOR (** *Numéro1 binaire* **, ** *Numéro2 binaire* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _nombre1 binaire_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Premier nombre binaire de 16 bits.  <br/> |
| _nombre2 binaire_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Deuxième nombre binaire de 16 bits.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Binaire de 16 bits
  
## <a name="example"></a>Exemple

BITOR(12,6)
  
Renvoie 14. Le 12 = 0...01100. Le 6 = 0...00110. Donc, BITOR(12,6) = 0...01110.
  

