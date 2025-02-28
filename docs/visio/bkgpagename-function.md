---
title: BKGPAGENAME, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253219
ms.localizationpriority: medium
ms.assetid: f6e410ef-54d5-9c08-926b-97a2a9786622
description: Renvoie un nom de page d’arrière-plan en tant que chaîne.
ms.openlocfilehash: 8a8361bf9be6c0f3534d4c6e83c5b33dac4d8dd6
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63402624"
---
# <a name="bkgpagename-function"></a>Fonction BKGPAGENAME

Renvoie un nom de page d’arrière-plan en tant que chaîne.
  
## <a name="syntax"></a>Syntaxe

BKGPAGENAME (***langID_opt*** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *langID_opt* <br/> |Facultatif  <br/> |**Numérique** <br/> |Permet de spécifier une langue pour la chaîne à laquelle la fonction renvoie. Utilisez 0 (valeur par défaut) pour spécifier la langue locale et 750 pour la langue universelle. |

### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

Si la page pour laquelle vous utilisez la fonction n’a pas de page d’arrière-plan, la chaîne «\<no background\> » est renvoyée.
  
Si vous utilisez un code de langue interdit, la langue locale est utilisée.
  