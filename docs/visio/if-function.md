---
title: IF, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251442
localization_priority: Normal
ms.assetid: 66771ad3-0fb3-68ff-81da-d1162d37c05a
description: Renvoie la valeur valeursivrai si l’expression logicalexpression a la valeur TRUE. Sinon, elle renvoie ValeurSiFaux.
ms.openlocfilehash: 55938e8bd78c02badb98f90665c5c26cdd70f3b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788810"
---
# <a name="if-function"></a>IF, fonction

Renvoie la _valeur valeursivrai_ si _l’expression logicalexpression_ a la valeur TRUE. Sinon, elle renvoie _ValeurSiFaux_.
  
## <a name="syntax"></a>Syntaxe

IF (** *logicalexpression* **, ** *renvoie ValeurSiVrai* **, ** *ValeurSiFaux* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _expression logicalexpression_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Expression à évaluer.  <br/> |
| _renvoie ValeurSiVrai_ <br/> |Obligatoire  <br/> |**Varie** <br/> |Valeur à renvoyer si _l’expression logicalexpression_ a la valeur true.  <br/> |
| _ValeurSiFaux_ <br/> |Obligatoire  <br/> |**Varie** <br/> | Valeur à renvoyer si _l’expression logicalexpression_ a la valeur false.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Variable
  
## <a name="example"></a>Exemple

IF (hauteur \> 1,25 dans, 5, 7)
  
Renvoie 5 si la hauteur de la forme est supérieure à 31,8 mm. Renvoie 7 si la hauteur de la forme est inférieure ou égale à 31,8 mm.
  

