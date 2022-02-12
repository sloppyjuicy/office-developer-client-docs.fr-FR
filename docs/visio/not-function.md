---
title: NOT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251469
ms.localizationpriority: medium
ms.assetid: 65873b32-2406-7c33-8e68-802461f467b2
description: Renvoie TRUE (1) si logicalexpression a la valeur FALSE. Sinon, elle renvoie FALSE (0).
ms.openlocfilehash: ef9a6b503c29e7609d78cb4282a5d0f21d592222
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62788828"
---
# <a name="not-function"></a>Fonction NOT

Renvoie TRUE (1) si  _logicalexpression_ a la valeur FALSE. Sinon, elle renvoie FALSE (0). 
  
## <a name="syntax"></a>Syntaxe

NOT(** *logicalexpression* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _logicalexpression_ <br/> |Requis  <br/> |**String** <br/> |Expression logique à évaluer |
   
### <a name="return-value"></a>Valeur renvoyée

Booléen
  
## <a name="example"></a>Exemple

NOT(Hauteur \> 0,75 « ) 
  
Renvoie 1 si la valeur de Hauteur est inférieure ou égale à 19,1 mm. Renvoie 0 si la valeur de Hauteur est supérieure à 19,1 mm. 
  

