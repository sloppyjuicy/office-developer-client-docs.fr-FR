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
ms.openlocfilehash: dcf3887ad3e7fa47f554983919b8c6ce714d68fd
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63404060"
---
# <a name="upper-function"></a>Fonction UPPER

Renvoie une chaîne convertie en minuscules.
  
## <a name="syntax"></a>Syntaxe

UPPER(***expression***)
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *expression* <br/> |Requis  <br/> |**Varie** <br/> | Chaîne, référence de cellule ou expression ; le résultat est converti en une chaîne à son tour convertie en majuscules. |

## <a name="remarks"></a>Remarques

La conversion dépend des paramètres régionaux et est basée sur les paramètres actuels de l’utilisateur.
  
## <a name="example"></a>Exemple

UPPER("mAJ eT Min")
  
Renvoie "MAJ ET MIN".
  