---
title: PATHSEGMENT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 08accf3b-93ac-9dd3-85ce-34ad42e79a4f
description: Renvoie le numéro de segment basé sur 1 à la marque de pourcentage spécifiée le long du chemin d’accès spécifié.
ms.openlocfilehash: 2e8646141e1ecfe28555ec998c574567f50b75fe
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63404691"
---
# <a name="pathsegment-function"></a>Fonction PATHSEGMENT

Renvoie le numéro de segment basé sur 1 à la marque de pourcentage spécifiée le long du chemin d’accès spécifié.
  
## <a name="syntax"></a>Syntaxe

PATHSEGMENT(***section** _, _*_travel_**)
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *section* <br/> |Requis  <br/> |**String** <br/> |Section Geometry qui représente le chemin, spécifiée par une référence à sa cellule Path (par exemple Geometry1.Path). |
| *travel* <br/> |Obligatoire  <br/> |**Double** <br/> |Pourcentage du chemin parcouru du point de début au point de fin. La valeur doit être comprise entre 0 et 1. |

### <a name="return-value"></a>Valeur renvoyée

Entier
  