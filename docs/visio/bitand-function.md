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
description: Renvoie un nombre binaire 16 bits dans lequel chaque bit est définie sur 1 uniquement si le bit correspondant dans binarynumber1 et binarynumber2 est 1. Dans le cas contraire, le bit est définie sur 0.
ms.openlocfilehash: a3c76a9122d0f02d5ab61460cf3457bb15da4d7b
ms.sourcegitcommit: 939bd9686ba41a8f94b82e004ed84b9054d9c7cf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/28/2020
ms.locfileid: "48293491"
---
# <a name="bitand-function"></a>Fonction BITAND

Renvoie un nombre binaire 16 bits dans lequel chaque bit est définie sur 1 uniquement si le bit correspondant dans binarynumber1 et binarynumber2 est 1. Dans le cas contraire, le bit est définie sur 0. 
  
## <a name="syntax"></a>Syntaxe

BITAND(***binarynumber1***, ***binarynumber2*** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _binary number1_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Premier nombre binaire de 16 bits.  <br/> |
| _binary number2_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Deuxième nombre binaire de 16 bits.  <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez utiliser cette fonction pour tester et modifier les propriétés d’une forme qui sont stockées sous forme de masque de bits, par exemple, le format de texte d’une forme.
  
## <a name="example"></a>Exemple

BITAND(12,6)
  
Renvoie 4. Le 12 = 0...01100. Le 6 = 0...00110. Donc, BITAND(12,6) = 0...00100.
  

