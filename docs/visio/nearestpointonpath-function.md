---
title: NEARESTPOINTONPATH, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 539bf79a-df09-2048-2aba-8c863dd26fc2
description: Renvoie le pourcentage de la distance le long du chemin du point le plus proche des coordonnées spécifiées, sous la forme d’une valeur comprise entre 0 et 1.
ms.openlocfilehash: 29c5dac690913c1b3715f18c4a661991ea4c23aa
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608227"
---
# <a name="nearestpointonpath-function"></a>Fonction NEARESTPOINTONPATH

Renvoie le pourcentage de la distance le long du chemin du point le plus proche des coordonnées spécifiées, sous la forme d’une valeur comprise entre 0 et 1.
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2010
 
  
## <a name="syntax"></a>Syntaxe

NEARESTPOINTONPATH(** *section* **, ** *x* **, ** *y* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Obligatoire  <br/> |**String** <br/> |Section Geometry qui représente le chemin, spécifiée par une référence à sa cellule Path (par exemple Geometry1.Path).  <br/> |
| _x_ <br/> |Obligatoire  <br/> |**Double** <br/> |Coordonnée  _x_ du point spécifié.  <br/> |
| _y_ <br/> |Obligatoire  <br/> |**Double** <br/> |Coordonnée  _y_ du point spécifié.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

 **Double**
  
## <a name="remarks"></a>Remarques

Si _la section_ n’existe pas, Microsoft Visio renvoie #REF!. 
  

