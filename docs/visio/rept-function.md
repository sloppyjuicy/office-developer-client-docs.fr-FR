---
title: REPT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027335
ms.localizationpriority: medium
ms.assetid: 53362a32-ac27-42a3-ace1-c6184ab20b52
description: Répète le texte un certain nombre de fois.
ms.openlocfilehash: 4a0741fc5ea15540d61d66d16004e5d0db5e381d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559653"
---
# <a name="rept-function"></a>Fonction REPT

Répète le texte un certain nombre de fois. 
  
## <a name="syntax"></a>Syntaxe

REPT (** *text* **, ** *number_times* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Obligatoire  <br/> |**String** <br/> | Texte à répéter.  <br/> |
| _number_times_ <br/> |Obligatoire  <br/> |**Number** <br/> |Valeur positive spécifiant le nombre de fois que le texte doit être répété.  <br/> |
   
## <a name="remarks"></a>Remarques

Si  *number_times*  est : 
  
- est zéro (0), REPT renvoie "" (texte vide) ;
    
- n’est pas un entier, il est tronqué.
    
## <a name="example"></a>Exemple

REPT ( » \* « , 5) 
  
Renvoie \* \* \* \* \* . 
  

