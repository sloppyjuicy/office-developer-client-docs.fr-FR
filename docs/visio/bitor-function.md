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
description: Renvoie un nombre binaire de 16 bits dans lequel chaque bit prend la valeur 1 si le bit correspondant dans nombre binaire1 ou nombre binaire2 est 1. Le bit est défini sur 0 uniquement si le bit correspondant est 0 dans le type binaire1 et le chiffre binaire2.
ms.openlocfilehash: 13bda2c6c65557b1f8372432cf919b2aaf2d75de
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303373"
---
# <a name="bitor-function"></a>Fonction BITOR

Renvoie un nombre binaire de 16 bits dans lequel chaque bit prend la valeur 1 si le bit correspondant dans nombre *binaire1* ou nombre *binaire2* est 1. Le bit est défini sur 0 uniquement si le bit correspondant est 0 dans le *type binaire1* et le chiffre *binaire2* . 
  
## <a name="syntax"></a>Syntaxe

BITOR (* * * * *binaire nombre1* * *, * * *binaires binaire2* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _valeurs binaire1 binaires_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Premier nombre binaire de 16 bits.  <br/> |
| _binaire binaire2_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Deuxième nombre binaire de 16 bits.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Binaire de 16 bits
  
## <a name="example"></a>Exemple

BITOR (12, 6)
  
Renvoie 14. Le 12 = 0...01100. Le 6 = 0...00110. Donc, BITOR(12,6) = 0...01110.
  

