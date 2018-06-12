---
title: REPT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027335
localization_priority: Normal
ms.assetid: 53362a32-ac27-42a3-ace1-c6184ab20b52
description: Répète un texte un certain nombre de fois.
ms.openlocfilehash: 761f2f95824d5bdab4995b2867bfeac6be64bc12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789497"
---
# <a name="rept-function"></a>REPT, fonction

Répète un texte un certain nombre de fois. 
  
## <a name="syntax"></a>Syntaxe

REPT (** *texte* **, ** *number_times* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> | Texte à répéter.  <br/> |
| _number_times_ <br/> |Obligatoire  <br/> |**Number** <br/> |Valeur positive spécifiant le nombre de fois que le texte doit être répété.  <br/> |
   
## <a name="remarks"></a>Note

Si *number_times :* 
  
- est zéro (0), REPT renvoie "" (texte vide) ;
    
- n’est pas un entier, il est tronqué.
    
## <a name="example"></a>Exemple

REPT («\*», 5) 
  
Cette propriété renvoie \* \* \* \* \*. 
  

