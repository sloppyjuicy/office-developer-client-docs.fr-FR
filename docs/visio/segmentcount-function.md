---
title: SEGMENTCOUNT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 792ec0e4-4a48-136b-904c-fe269e355070
description: Renvoie le nombre de segments qui constituent le chemin.
ms.openlocfilehash: 93a77d9085e6900f502a75401847ad685d25effd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789622"
---
# <a name="segmentcount-function"></a>SEGMENTCOUNT, fonction

Renvoie le nombre de segments qui constituent le chemin.
  
## <a name="syntax"></a>Syntaxe

SEGMENTCOUNT (** *pathRef* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _pathRef_ <br/> |Obligatoire  <br/> |**Integer** <br/> |Section Geometry qui représente le chemin, spécifiée par une référence à sa cellule Path (par exemple Geometry1.Path).  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Entier
  
## <a name="remarks"></a>Remarques

Le total des segments renvoyés ne tient pas compte des déviations de trait.
  

