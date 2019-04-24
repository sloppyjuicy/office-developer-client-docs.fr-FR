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
description: Renvoie un nombre binaire de 16 bits dans lequel chaque bit prend la valeur 1 si le bit correspondant dans l'un ou l'autre des nombres binaire1 et binaire2 est 1. Dans le cas contraire, le bit prend la valeur 0.
ms.openlocfilehash: ab8ff46fe98512d963ef4ecd5c37127353827725
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302988"
---
# <a name="bitxor-function"></a>Fonction BITXOR

Renvoie un nombre binaire de 16 bits dans lequel chaque bit prend la valeur 1 si le bit correspondant dans l'un ou l'autre des nombres binaire1 et binaire2 est 1. Dans le cas contraire, le bit prend la valeur 0.
  
## <a name="syntax"></a>Syntaxe

BITXOR (* * * * *binaire nombre1* * *, * * *binaires binaire2* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _valeurs binaire1 binaires_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Premier nombre binaire de 16 bits.  <br/> |
| _binaire binaire2_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Deuxième nombre binaire de 16 bits.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Binaire de 16 bits
  
## <a name="example"></a>Exemple

BITXOR (12, 6)
  
Renvoie 10. Le 12 = 0...01100. Le 6 = 0...00110. Donc, BITXOR(12,6) = 0...01010.
  

