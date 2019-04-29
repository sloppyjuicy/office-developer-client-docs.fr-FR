---
title: BKGPAGENAME, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253219
localization_priority: Normal
ms.assetid: f6e410ef-54d5-9c08-926b-97a2a9786622
description: Renvoie un nom de page d'arrière-plan sous forme de chaîne.
ms.openlocfilehash: 3b628315052117fe853c8f9c0fc36572de25d871
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410314"
---
# <a name="bkgpagename-function"></a>Fonction BKGPAGENAME

Renvoie un nom de page d'arrière-plan sous forme de chaîne.
  
## <a name="syntax"></a>Syntaxe

BKGPAGENAME (* * *langID_opt* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _langID_opt_ <br/> |Facultatif  <br/> |**Numérique** <br/> |Permet de spécifier une langue pour la chaîne à laquelle la fonction renvoie. Utilisez 0 (valeur par défaut) pour spécifier la langue locale et 750 pour la langue universelle.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

Si la page pour laquelle vous utilisez la fonction n'a pas de page d'arrière-plan,\<la chaîne\>«aucun arrière-plan» est renvoyée. 
  
Si vous utilisez un code de langue interdit, la langue locale est utilisée. 
  

