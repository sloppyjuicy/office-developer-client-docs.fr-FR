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
description: Répète le texte un certain nombre de fois.
ms.openlocfilehash: 84e7167fcee426c607e6967aff0530362685dd35
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412078"
---
# <a name="rept-function"></a>Fonction REPT

Répète le texte un certain nombre de fois. 
  
## <a name="syntax"></a>Syntaxe

REPT (* * *texte* * *, * * *no_fois* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Obligatoire  <br/> |**String** <br/> | Texte à répéter.  <br/> |
| _no_fois_ <br/> |Obligatoire  <br/> |**Number** <br/> |Valeur positive spécifiant le nombre de fois que le texte doit être répété.  <br/> |
   
## <a name="remarks"></a>Remarques

Si *no_fois* est: 
  
- est zéro (0), REPT renvoie "" (texte vide) ;
    
- n’est pas un entier, il est tronqué.
    
## <a name="example"></a>Exemple

REPT ("\*", 5) 
  
\* \*Renvoie \*. \* \* 
  

