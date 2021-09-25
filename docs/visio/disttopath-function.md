---
title: DISTTOPATH, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 2ba7d372-0c2a-9fa7-0af6-97da0aafdb12
description: Renvoie la distance la plus courte entre le point représenté par les coordonnées spécifiées et un point du chemin.
ms.openlocfilehash: f6e0bae491b148c16ae4e0f87edd02cc9d4b9f9d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586543"
---
# <a name="disttopath-function"></a>Fonction DISTTOPATH

Renvoie la distance la plus courte entre le point représenté par les coordonnées spécifiées et un point du chemin.
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2010
 
  
## <a name="syntax"></a>Syntaxe

DISTTOPATH(** *section* **, ** *x* **, ** *y* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Obligatoire  <br/> |**String** <br/> |Section Geometry qui représente le chemin, spécifiée par une référence à sa cellule Path (par exemple Geometry1.Path).  <br/> |
| _x_ <br/> |Obligatoire  <br/> |**Double** <br/> |Coordonnée  _x_ du point.  <br/> |
| _y_ <br/> |Obligatoire  <br/> |**Double** <br/> |Coordonnée  _y_ du point.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

 **Double**
  
## <a name="remarks"></a>Remarques

Microsoft Visio renvoie #REF! si  _la section_ n’existe pas. 
  
La valeur renvoyée est positive si le point se situe à gauche par rapport au sens de déplacement, et négative s’il se situe à droite.
  

