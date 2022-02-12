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
ms.openlocfilehash: b6c2eebc3acec6fb95387538b583c3d005c7aedb
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62772696"
---
# <a name="rept-function"></a>Fonction REPT

Répète le texte un certain nombre de fois. 
  
## <a name="syntax"></a>Syntaxe

REPT (** *text* **, ** *number_times* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Requis  <br/> |**String** <br/> | Texte à répéter. |
| _number_times_ <br/> |Requis  <br/> |**Number** <br/> |Valeur positive spécifiant le nombre de fois que le texte doit être répété. |
   
## <a name="remarks"></a>Remarques

Si  *number_times*  est : 
  
- est zéro (0), REPT renvoie "" (texte vide) ;
    
- n’est pas un entier, il est tronqué.
    
## <a name="example"></a>Exemple

REPT (« \* », 5) 
  
Renvoie \*\*\*\*\*. 
  

