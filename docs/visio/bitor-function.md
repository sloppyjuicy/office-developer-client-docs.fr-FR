---
title: BITOR, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251400
ms.localizationpriority: medium
ms.assetid: 1d0954c5-b2cb-6c5d-62b3-a68011cf0c85
description: Renvoie un nombre binaire 16 bits dans lequel chaque bit est définie sur 1 si le bit correspondant dans le nombre binaire numéro1 ou le nombre binaire2 est 1. Le bit est définie sur 0 uniquement si le bit correspondant est 0 dans le nombre binaire 1 et le nombre binaire 2 .
ms.openlocfilehash: 6f6e6176e2e14291547db31514fd105622a44fd4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616018"
---
# <a name="bitor-function"></a>Fonction BITOR

Renvoie un nombre binaire 16 bits dans lequel chaque bit est définie sur 1 si le bit correspondant dans le nombre  *binaire numéro1*  ou le nombre  *binaire2*  est 1. Le bit est définie sur 0 uniquement si le bit correspondant est 0 dans le  *nombre binaire 1*  et  *le nombre binaire 2*  . 
  
## <a name="syntax"></a>Syntaxe

BITOR(** *binary number1* **, ** *binary number2* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _binary number1_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Premier nombre binaire de 16 bits.  <br/> |
| _binary number2_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Deuxième nombre binaire de 16 bits.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Binaire de 16 bits
  
## <a name="example"></a>Exemple

BITOR(12,6)
  
Renvoie 14. Le 12 = 0...01100. Le 6 = 0...00110. Donc, BITOR(12,6) = 0...01110.
  

