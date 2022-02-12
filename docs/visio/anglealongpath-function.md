---
title: ANGLEALONGPATH, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: d7f8ca9a-3a89-abab-9805-bd1e24075c3f
description: Renvoie l’angle de la tangente du chemin à un point donné.
ms.openlocfilehash: 95368a5b69a07e47d49f43df758c3cd20e2bdea7
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62774600"
---
# <a name="anglealongpath-function"></a>Fonction ANGLEALONGPATH

Renvoie l’angle de la tangente du chemin à un point donné.
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2010
 
  
## <a name="syntax"></a>Syntaxe

ANGLEALONGPATH(***section**_, _*_travel_*_ _*_[,segment]_** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Requis  <br/> |**String** <br/> |Section Geometry qui représente le chemin, spécifiée par une référence à sa cellule Path (par exemple Geometry1.Path). |
| _travel_ <br/> |Obligatoire  <br/> |**Double** <br/> |Pourcentage le long du chemin du point de début au point de fin. La valeur doit être comprise entre 0 et 1. |
| _segment_ <br/> |Facultatif  <br/> |**Integer** <br/> |Segment de base 1 du chemin sur lequel calculer l’angle de la tangente. |
   
### <a name="return-value"></a>Valeur renvoyée

 **Double**
  
## <a name="remarks"></a>Remarques

Si vous incluez une valeur  _de segment_ , ANGLEALONGPATH renvoie la valeur de ce segment uniquement. 
  
Si vous incluez une valeur  _de segment_ , ANGLEALONGPATH détermine le point de la tangente à l’aide de  _travel_ pour calculer la séquence le long du  _segment_.
  
Si _l’une ou_ _l’autre section ou segment_ n’existe pas, Microsoft Visio renvoie #REF!. 
  

