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
ms.openlocfilehash: 6c9db7a5820a543f4dbe26d27094f858606917e6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623284"
---
# <a name="pagename-function"></a>Fonction PAGENAME

Renvoie le nom de la page sous la mesure d’une chaîne.
  
## <a name="syntax"></a>Syntaxe

PAGENAME (** *langID_opt* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _langID_opt_ <br/> |Facultatif  <br/> |**Number** <br/> |Permet de spécifier une langue pour la chaîne à laquelle la fonction renvoie. Utilisez 0 (valeur par défaut) pour spécifier la langue locale et 750 pour la langue universelle.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

Si vous utilisez un code de langue interdit, la langue locale est utilisée.
  

