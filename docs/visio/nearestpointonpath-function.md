---
title: NEARESTPOINTONPATH, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 539bf79a-df09-2048-2aba-8c863dd26fc2
description: Renvoie le pourcentage de la distance le long du chemin du point le plus proche des coordonnées spécifiées, sous la forme d’une valeur comprise entre 0 et 1.
ms.openlocfilehash: f6cfecd19be0f45e5b9a08e7ec1526d3f6d1489d
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63368950"
---
# <a name="nearestpointonpath-function"></a>Fonction NEARESTPOINTONPATH

Renvoie le pourcentage de la distance le long du chemin du point le plus proche des coordonnées spécifiées, sous la forme d’une valeur comprise entre 0 et 1.
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2010
 
  
## <a name="syntax"></a>Syntaxe

NEARESTPOINTONPATH(***section** _, _*_x_*_, _ *_y_** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Requis  <br/> |**String** <br/> |Section Geometry qui représente le chemin, spécifiée par une référence à sa cellule Path (par exemple Geometry1.Path). |
| _x_ <br/> |Obligatoire  <br/> |**Double** <br/> |Coordonnée  _x_ du point spécifié. |
| _y_ <br/> |Obligatoire  <br/> |**Double** <br/> |Coordonnée  _y_ du point spécifié. |
   
### <a name="return-value"></a>Valeur renvoyée

 **Double**
  
## <a name="remarks"></a>Remarques

Si _la section_ n’existe pas, Microsoft Visio renvoie #REF!. 
  

