---
title: PATHSEGMENT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 08accf3b-93ac-9dd3-85ce-34ad42e79a4f
description: Renvoie le numéro de segment basé sur 1 à la marque de pourcentage spécifiée le long du chemin d’accès spécifié.
ms.openlocfilehash: 3db8c434254aef11df5edbaca0f2ceeea25003a6
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62777137"
---
# <a name="pathsegment-function"></a>Fonction PATHSEGMENT

Renvoie le numéro de segment basé sur 1 à la marque de pourcentage spécifiée le long du chemin d’accès spécifié.
  
## <a name="syntax"></a>Syntaxe

PATHSEGMENT(** *section* **, ** *travel* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Requis  <br/> |**String** <br/> |Section Geometry qui représente le chemin, spécifiée par une référence à sa cellule Path (par exemple Geometry1.Path). |
| _travel_ <br/> |Obligatoire  <br/> |**Double** <br/> |Pourcentage du chemin parcouru du point de début au point de fin. La valeur doit être comprise entre 0 et 1. |
   
### <a name="return-value"></a>Valeur renvoyée

Entier
  

