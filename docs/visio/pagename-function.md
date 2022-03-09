---
title: PAGENAME, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251577
ms.localizationpriority: medium
ms.assetid: 12e45f46-e773-9445-4c7f-c726ab648671
description: Renvoie le nom de la page sous la mesure d’une chaîne.
ms.openlocfilehash: 3993a005e941ee1ae80ad4d0db9e14f6ef22c0c3
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63404438"
---
# <a name="pagename-function"></a>Fonction PAGENAME

Renvoie le nom de la page sous la mesure d’une chaîne.
  
## <a name="syntax"></a>Syntaxe

PAGENAME (***langID_opt***)
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *langID_opt* <br/> |Facultatif  <br/> |**Number** <br/> |Permet de spécifier une langue pour la chaîne à laquelle la fonction renvoie. Utilisez 0 (valeur par défaut) pour spécifier la langue locale et 750 pour la langue universelle. |

### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

Si vous utilisez un code de langue interdit, la langue locale est utilisée.
  