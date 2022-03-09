---
title: SEGMENTCOUNT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 792ec0e4-4a48-136b-904c-fe269e355070
description: Renvoie le nombre de segments qui constituent le chemin.
ms.openlocfilehash: fbf1ea3fa0588065fd9f13b68e7cc1b4e9ce27fa
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63404550"
---
# <a name="segmentcount-function"></a>Fonction SEGMENTCOUNT

Renvoie le nombre de segments qui constituent le chemin.
  
## <a name="syntax"></a>Syntaxe

SEGMENTCOUNT(***pathRef***)
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *pathRef* <br/> |Obligatoire  <br/> |**Entier** <br/> |Section Geometry qui représente le chemin, spécifiée par une référence à sa cellule Path (par exemple Geometry1.Path). |

### <a name="return-value"></a>Valeur renvoyée

Entier
  
## <a name="remarks"></a>Remarques

Le total des segments renvoyés ne tient pas compte des déviations de trait.
  