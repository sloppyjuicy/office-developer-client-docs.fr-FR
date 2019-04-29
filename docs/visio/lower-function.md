---
title: LOWER, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251459
localization_priority: Normal
ms.assetid: 1d198ea6-49e0-e462-b2cf-b65fbb920b55
description: Renvoie une chaîne convertie en minuscules.
ms.openlocfilehash: 275e5cc40bed5c3ca7d6f40b0882f523334611c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421241"
---
# <a name="lower-function"></a>Fonction LOWER

Renvoie une chaîne convertie en minuscules.
  
## <a name="syntax"></a>Syntaxe

LOWER (* * *expression* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Obligatoire  <br/> |**Réelle** <br/> | Chaîne, référence de cellule ou expression ; le résultat est converti en une chaîne à son tour convertie en minuscules.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

La conversion dépend des paramètres régionaux et est basée sur les paramètres actuels de l’utilisateur. 
  
## <a name="example"></a>Exemple

LOWER("mAJ eT Min") 
  
Renvoie « maj et min ». 
  

