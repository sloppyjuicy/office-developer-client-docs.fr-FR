---
title: NAME, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251580
ms.localizationpriority: medium
ms.assetid: 1ca67a09-9df2-37f5-b269-e761d76bb011
description: Renvoie le nom d’une feuille en tant que chaîne.
ms.openlocfilehash: 3d37fce198da658fce93191ff21485217f3f6ae2
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62788842"
---
# <a name="name-function"></a>Fonction NAME

Renvoie le nom d’une feuille en tant que chaîne.
  
## <a name="syntax"></a>Syntaxe

NAME (** *langID_opt* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _langID_opt_ <br/> |Facultatif  <br/> |**Number** <br/> |Permet de spécifier une langue pour la chaîne à laquelle la fonction renvoie. Utilisez 0 (valeur par défaut) pour spécifier la langue locale et 750 pour la langue universelle. |
   
### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

Si vous utilisez un code de langue interdit, la langue locale est utilisée. 
  

