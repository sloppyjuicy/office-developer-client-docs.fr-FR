---
title: DISTTOPATH, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2ba7d372-0c2a-9fa7-0af6-97da0aafdb12
description: Renvoie la distance la plus courte entre le point représenté par les coordonnées spécifiées et un point du chemin.
ms.openlocfilehash: 5727b24739705d3e562150c48fe77f7ad6eedb57
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332689"
---
# <a name="disttopath-function"></a>Fonction DISTTOPATH

Renvoie la distance la plus courte entre le point représenté par les coordonnées spécifiées et un point du chemin.
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2010
 
  
## <a name="syntax"></a>Syntaxe

DISTTOPATH (* * *section* * *, * * *x* * *, * * *y* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Obligatoire  <br/> |**String** <br/> |Section Geometry qui représente le chemin, spécifiée par une référence à sa cellule Path (par exemple Geometry1.Path).  <br/> |
| _x_ <br/> |Obligatoire  <br/> |**Double** <br/> |Coordonnée _x_du point.  <br/> |
| _y_ <br/> |Obligatoire  <br/> |**Double** <br/> |Coordonnée _y_du point.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

 **Double**
  
## <a name="remarks"></a>Remarques

Microsoft Visio renvoie #REF! Si la _section_ n'existe pas. 
  
La valeur renvoyée est positive si le point se situe à gauche par rapport au sens de déplacement, et négative s’il se situe à droite.
  

