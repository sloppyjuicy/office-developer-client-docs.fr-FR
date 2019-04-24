---
title: NAME, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251580
localization_priority: Normal
ms.assetid: 1ca67a09-9df2-37f5-b269-e761d76bb011
description: Renvoie le nom d'une feuille sous forme de chaîne.
ms.openlocfilehash: 7d0a4e9f3c5f70be07e9cc5691f52afcbc7bea68
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319424"
---
# <a name="name-function"></a>Fonction NAME

Renvoie le nom d'une feuille sous forme de chaîne.
  
## <a name="syntax"></a>Syntaxe

NOM (* * *langID_opt* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _langID_opt_ <br/> |Facultatif  <br/> |**Number** <br/> |Permet de spécifier une langue pour la chaîne à laquelle la fonction renvoie. Utilisez 0 (valeur par défaut) pour spécifier la langue locale et 750 pour la langue universelle.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

Si vous utilisez un code de langue interdit, la langue locale est utilisée. 
  

