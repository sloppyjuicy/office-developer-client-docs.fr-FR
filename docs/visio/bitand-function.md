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
description: Renvoie un nombre binaire de 16 bits dans lequel chaque bit est défini sur 1 uniquement si le bit correspondant dans binarynumber1 et binarynumber2 est 1. Dans le cas contraire, le bit prend la valeur 0.
ms.openlocfilehash: 495ad645a422c0333d02a22c3c600dd1e0d567bd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409726"
---
# <a name="bitand-function"></a>Fonction BITAND

Renvoie un nombre binaire de 16 bits dans lequel chaque bit est défini sur 1 uniquement si le bit correspondant dans binarynumber1 et binarynumber2 est 1. Dans le cas contraire, le bit prend la valeur 0. 
  
## <a name="syntax"></a>Syntaxe

BITAND (* * *binarynumber1* * *, * * *binarynumber2* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _valeurs binaire1 binaires_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Premier nombre binaire de 16 bits.  <br/> |
| _binaire binaire2_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Deuxième nombre binaire de 16 bits.  <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez utiliser cette fonction pour tester et modifier les propriétés d’une forme qui sont stockées sous forme de masque de bits, par exemple, le format de texte d’une forme.
  
## <a name="example"></a>Exemple

BITAND (12, 6)
  
Renvoie 4. Le 12 = 0...01100. Le 6 = 0...00110. Donc, BITAND(12,6) = 0...00100.
  

