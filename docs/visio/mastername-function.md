---
title: MASTERNAME, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251581
ms.localizationpriority: medium
ms.assetid: 519d79d4-9178-2231-c26d-aa7f31a43412
description: Renvoie le nom de la feuille en tant que chaîne, ou renvoie la chaîne « no master » si la feuille n’a pas de master.
ms.openlocfilehash: 51e984edea037d4cb1de6b2b9617978a132e0198
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63405615"
---
# <a name="mastername-function"></a>Fonction MASTERNAME

Renvoie le nom de la feuille en tant que chaîne ou la chaîne «\<no master\> » si la feuille n’a pas de master.
  
## <a name="syntax"></a>Syntaxe

MASTERNAME ([ ***langID_opt*** ])
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *langID_opt* <br/> |Facultatif  <br/> |**Number** <br/> |Permet de spécifier une langue pour la chaîne à laquelle la fonction renvoie. Utilisez 0 (valeur par défaut) pour spécifier la langue locale et 750 pour la langue universelle. |

### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

Si vous utilisez un code de langue interdit, la langue locale est utilisée.
  