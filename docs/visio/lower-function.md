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
ms.openlocfilehash: 911bf2f57630245f8377b402d539d4311ac65afc
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63405650"
---
# <a name="lower-function"></a>Fonction LOWER

Renvoie une chaîne convertie en minuscules.
  
## <a name="syntax"></a>Syntaxe

LOWER(***expression***)
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *expression* <br/> |Requis  <br/> |**Varie** <br/> | Chaîne, référence de cellule ou expression ; le résultat est converti en une chaîne à son tour convertie en minuscules. |

### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

La conversion dépend des paramètres régionaux et est basée sur les paramètres actuels de l’utilisateur.
  
## <a name="example"></a>Exemple

LOWER("mAJ eT Min")
  
Renvoie « maj et min ».
  