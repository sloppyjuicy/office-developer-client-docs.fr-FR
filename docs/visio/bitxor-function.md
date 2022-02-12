---
title: BITXOR, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251401
ms.localizationpriority: medium
ms.assetid: 672eacaf-a374-c7e2-b39b-8d42d2371aee
description: Renvoie un nombre binaire 16 bits dans lequel chaque bit est définie sur 1 si le bit correspondant dans l’un ou l’autre, mais pas dans le nombre binaire number1 et le nombre binaire 2, est 1. Dans le cas contraire, le bit est définie sur 0.
ms.openlocfilehash: e3ab1da01ee01b5c8c249391429a3e39da8cc611
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62778628"
---
# <a name="bitxor-function"></a>Fonction BITXOR

Renvoie un nombre binaire 16 bits dans lequel chaque bit est définie sur 1 si le bit correspondant dans l’un ou l’autre, mais pas dans le nombre binaire number1 et le nombre binaire 2, est 1. Dans le cas contraire, le bit est définie sur 0.
  
## <a name="syntax"></a>Syntaxe

BITXOR(** *binary number1* **, ** *binary number2* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _binary number1_ <br/> |Requis  <br/> |**Numérique** <br/> |Premier nombre binaire de 16 bits. |
| _binary number2_ <br/> |Requis  <br/> |**Numérique** <br/> |Deuxième nombre binaire de 16 bits. |
   
### <a name="return-value"></a>Valeur renvoyée

Binaire de 16 bits
  
## <a name="example"></a>Exemple

BITXOR(12,6)
  
Renvoie 10. Le 12 = 0...01100. Le 6 = 0...00110. Donc, BITXOR(12,6) = 0...01010.
  

