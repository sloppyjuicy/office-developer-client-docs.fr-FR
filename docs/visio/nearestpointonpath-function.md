---
title: NEARESTPOINTONPATH, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 539bf79a-df09-2048-2aba-8c863dd26fc2
description: Renvoie le pourcentage de la distance le long du chemin du point le plus proche des coordonnées spécifiées, sous la forme d’une valeur comprise entre 0 et 1.
ms.openlocfilehash: ced20cdf1f3531eafaa03c2666b09334029fd3da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319718"
---
# <a name="nearestpointonpath-function"></a>Fonction NEARESTPOINTONPATH

Renvoie le pourcentage de la distance le long du chemin du point le plus proche des coordonnées spécifiées, sous la forme d’une valeur comprise entre 0 et 1.
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2010
 
  
## <a name="syntax"></a>Syntaxe

NEARESTPOINTONPATH (* * *section* * *, * * *x* * *, * * *y* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Obligatoire  <br/> |**String** <br/> |Section Geometry qui représente le chemin, spécifiée par une référence à sa cellule Path (par exemple Geometry1.Path).  <br/> |
| _x_ <br/> |Obligatoire  <br/> |**Double** <br/> |Coordonnée _x_du point spécifié.  <br/> |
| _y_ <br/> |Obligatoire  <br/> |**Double** <br/> |Coordonnée _y_du point spécifié.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

 **Double**
  
## <a name="remarks"></a>Remarques

Si _section_ n'existe pas, Microsoft Visio renvoie #REF!. 
  

