---
title: NOT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251469
localization_priority: Normal
ms.assetid: 65873b32-2406-7c33-8e68-802461f467b2
description: Renvoie TRUE (1) si logicalexpression a la valeur FALSE. Sinon, elle renvoie FALSE (0).
ms.openlocfilehash: 3359e21654bcc318caf31405093f851eca064119
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413331"
---
# <a name="not-function"></a>Fonction NOT

Renvoie TRUE (1) si  _logicalexpression_ a la valeur FALSE. Sinon, elle renvoie FALSE (0). 
  
## <a name="syntax"></a>Syntaxe

NOT(** *logicalexpression* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _logicalexpression_ <br/> |Obligatoire  <br/> |**String** <br/> |Expression logique à évaluer  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Booléen
  
## <a name="example"></a>Exemple

NOT(Hauteur \> 0,75 cm) 
  
Renvoie 1 si la valeur de Hauteur est inférieure ou égale à 19,1 mm. Renvoie 0 si la valeur de Hauteur est supérieure à 19,1 mm. 
  

