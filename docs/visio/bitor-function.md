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
description: Renvoie un nombre binaire 16 bits dans lequel chaque bit est définie sur 1 si le bit correspondant dans le nombre binaire 1 ou le nombre binaire 2 est 1. Le bit est définie sur 0 uniquement si le bit correspondant est 0 dans le nombre binaire 1 et le nombre binaire2 .
ms.openlocfilehash: 8cbc0624e83a359436ca18e6f560857fbf490038
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62783627"
---
# <a name="bitor-function"></a>Fonction BITOR

Renvoie un nombre binaire 16 bits dans lequel chaque bit est définie sur 1 si le bit correspondant dans le nombre  *binaire 1*  ou le nombre  *binaire 2*  est 1. Le bit est définie sur 0 uniquement si le bit correspondant est 0 dans le  *nombre binaire 1*  et  *le nombre binaire2*  . 
  
## <a name="syntax"></a>Syntaxe

BITOR(** *binary number1* **, ** *binary number2* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _binary number1_ <br/> |Requis  <br/> |**Numérique** <br/> |Premier nombre binaire de 16 bits. |
| _binary number2_ <br/> |Requis  <br/> |**Numérique** <br/> |Deuxième nombre binaire de 16 bits. |
   
### <a name="return-value"></a>Valeur renvoyée

Binaire de 16 bits
  
## <a name="example"></a>Exemple

BITOR(12,6)
  
Renvoie 14. Le 12 = 0...01100. Le 6 = 0...00110. Donc, BITOR(12,6) = 0...01110.
  

