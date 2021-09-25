---
title: ANGLEALONGPATH, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: d7f8ca9a-3a89-abab-9805-bd1e24075c3f
description: Renvoie l’angle de la tangente du chemin à un point donné.
ms.openlocfilehash: c7b82a32820de6a0f1faacc8dcf990edb202ca84
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578248"
---
# <a name="anglealongpath-function"></a>Fonction ANGLEALONGPATH

Renvoie l’angle de la tangente du chemin à un point donné.
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2010
 
  
## <a name="syntax"></a>Syntaxe

ANGLEALONGPATH(***section**_, _*_travel_*_ _*_ [,segment]_** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Obligatoire  <br/> |**String** <br/> |Section Geometry qui représente le chemin, spécifiée par une référence à sa cellule Path (par exemple Geometry1.Path).  <br/> |
| _travel_ <br/> |Obligatoire  <br/> |**Double** <br/> |Pourcentage le long du chemin du point de début au point de fin. La valeur doit être comprise entre 0 et 1.  <br/> |
| _segment_ <br/> |Facultatif  <br/> |**Integer** <br/> |Segment de base 1 du chemin sur lequel calculer l’angle de la tangente.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

 **Double**
  
## <a name="remarks"></a>Remarques

Si vous incluez une valeur  _de segment,_ ANGLEALONGPATH renvoie la valeur de ce segment uniquement. 
  
Si vous incluez une valeur  _de segment,_ ANGLEALONGPATH détermine le point de la tangente à l’aide de  _travel_ pour calculer la séquence le long du  _segment_.
  
Si _l’une ou_ _l’autre section_ ou segment n’existe pas, Microsoft Visio renvoie #REF!. 
  

