---
title: UPPER, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251509
ms.localizationpriority: medium
ms.assetid: ef94ee0f-dbb8-a2e1-1805-8a6609830d2a
description: Renvoie une chaîne convertie en minuscules.
ms.openlocfilehash: aad79f5b04f94bcfe12615d6e0498fbf501f0e49
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622668"
---
# <a name="upper-function"></a>Fonction UPPER

Renvoie une chaîne convertie en minuscules.
  
## <a name="syntax"></a>Syntaxe

UPPER(** *expression* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Obligatoire  <br/> |**Varie** <br/> | Chaîne, référence de cellule ou expression ; le résultat est converti en une chaîne à son tour convertie en majuscules.  <br/> |
   
## <a name="remarks"></a>Remarques

La conversion dépend des paramètres régionaux et est basée sur les paramètres actuels de l’utilisateur. 
  
## <a name="example"></a>Exemple

UPPER("mAJ eT Min") 
  
Renvoie "MAJ ET MIN". 
  

