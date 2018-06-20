---
title: BITXOR, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251401
localization_priority: Normal
ms.assetid: 672eacaf-a374-c7e2-b39b-8d42d2371aee
description: Renvoie un nombre binaire de 16 bits dans lequel chaque bit a la valeur 1 si le bit correspondant dans soit binaire Numéro1 et numéro2 binaire est 1. Sinon, le bit est défini sur 0.
ms.openlocfilehash: a0e03258bcfe694dc3bec5469095eff90fb94f1a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788130"
---
# <a name="bitxor-function"></a>BITXOR, fonction

Renvoie un nombre binaire de 16 bits dans lequel chaque bit a la valeur 1 si le bit correspondant dans soit binaire Numéro1 et numéro2 binaire est 1. Sinon, le bit est défini sur 0.
  
## <a name="syntax"></a>Syntaxe

BITXOR (** *Numéro1 binaire* **, ** *Numéro2 binaire* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _nombre1 binaire_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Premier nombre binaire de 16 bits.  <br/> |
| _nombre2 binaire_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Deuxième nombre binaire de 16 bits.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Binaire de 16 bits
  
## <a name="example"></a>Exemple

BITXOR(12,6)
  
Renvoie 10. Le 12 = 0...01100. Le 6 = 0...00110. Donc, BITXOR(12,6) = 0...01010.
  

