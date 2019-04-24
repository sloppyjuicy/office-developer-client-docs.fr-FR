---
title: PATHSEGMENT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 08accf3b-93ac-9dd3-85ce-34ad42e79a4f
description: Renvoie le numéro de segment basé sur 1 à la marque de pourcentage spécifiée le long du chemin d'accès spécifié.
ms.openlocfilehash: c4dfc4d33de1a9c1a03ef14d76103b4de0f28bc7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344449"
---
# <a name="pathsegment-function"></a>Fonction PATHSEGMENT

Renvoie le numéro de segment basé sur 1 à la marque de pourcentage spécifiée le long du chemin d'accès spécifié.
  
## <a name="syntax"></a>Syntaxe

PATHSEGMENT (* * *section* * *, * * *voyages* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Obligatoire  <br/> |**String** <br/> |Section Geometry qui représente le chemin, spécifiée par une référence à sa cellule Path (par exemple Geometry1.Path).  <br/> |
| _poche_ <br/> |Obligatoire  <br/> |**Double** <br/> |Pourcentage du chemin parcouru du point de début au point de fin. La valeur doit être comprise entre 0 et 1.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Entier
  

