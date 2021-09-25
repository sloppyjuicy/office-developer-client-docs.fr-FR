---
title: LOWER, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251459
ms.localizationpriority: medium
ms.assetid: 1d198ea6-49e0-e462-b2cf-b65fbb920b55
description: Renvoie une chaîne convertie en minuscules.
ms.openlocfilehash: 4021eb5952a3718e74e8e1c16f72268d08ae3832
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615857"
---
# <a name="lower-function"></a>Fonction LOWER

Renvoie une chaîne convertie en minuscules.
  
## <a name="syntax"></a>Syntaxe

LOWER(** *expression* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Obligatoire  <br/> |**Varie** <br/> | Chaîne, référence de cellule ou expression ; le résultat est converti en une chaîne à son tour convertie en minuscules.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

La conversion dépend des paramètres régionaux et est basée sur les paramètres actuels de l’utilisateur. 
  
## <a name="example"></a>Exemple

LOWER("mAJ eT Min") 
  
Renvoie « maj et min ». 
  

