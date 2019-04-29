---
title: SEGMENTCOUNT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 792ec0e4-4a48-136b-904c-fe269e355070
description: Renvoie le nombre de segments qui constituent le chemin.
ms.openlocfilehash: 947e37c13de638e4f281bc17376a253a8ca07e04
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424496"
---
# <a name="segmentcount-function"></a>Fonction SEGMENTCOUNT

Renvoie le nombre de segments qui constituent le chemin.
  
## <a name="syntax"></a>Syntaxe

SEGMENTCOUNT (* * *pathRef* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _pathRef_ <br/> |Obligatoire  <br/> |**Entier** <br/> |Section Geometry qui représente le chemin, spécifiée par une référence à sa cellule Path (par exemple Geometry1.Path).  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Entier
  
## <a name="remarks"></a>Remarques

Le total des segments renvoyés ne tient pas compte des déviations de trait.
  

