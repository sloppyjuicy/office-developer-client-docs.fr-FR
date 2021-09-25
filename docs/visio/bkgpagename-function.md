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
ms.openlocfilehash: 96e475690fafee2aba534419578428ad96320e3f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554844"
---
# <a name="bkgpagename-function"></a>Fonction BKGPAGENAME

Renvoie un nom de page d’arrière-plan en tant que chaîne.
  
## <a name="syntax"></a>Syntaxe

BKGPAGENAME (** *langID_opt* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _langID_opt_ <br/> |Facultatif  <br/> |**Numérique** <br/> |Permet de spécifier une langue pour la chaîne à laquelle la fonction renvoie. Utilisez 0 (valeur par défaut) pour spécifier la langue locale et 750 pour la langue universelle.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

Si la page pour laquelle vous utilisez la fonction n’a pas de page d’arrière-plan, la chaîne \<no background\> « » est renvoyée. 
  
Si vous utilisez un code de langue interdit, la langue locale est utilisée. 
  

