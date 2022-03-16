---
title: ANGLEALONGPATH, fonction
manager: lindalu
ms.date: 03/09/2022
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: d7f8ca9a-3a89-abab-9805-bd1e24075c3f
description: Renvoie l’angle de la tangente du chemin à un point donné.
ms.openlocfilehash: 2907698164817642b5bcbaae8868f920a0092d87
ms.sourcegitcommit: b2c5a02b2d0abd2da2542089fc3f83ff07e121e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2022
ms.locfileid: "63507679"
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
| *section* <br/> |Requis  <br/> |**String** <br/> |Section Geometry qui représente le chemin, spécifiée par une référence à sa cellule Path (par exemple Geometry1.Path). |
| *travel* <br/> |Obligatoire  <br/> |**Double** <br/> |Pourcentage le long du chemin du point de début au point de fin. La valeur doit être comprise entre 0 et 1. |
| *segment* <br/> |Facultatif  <br/> |**Integer** <br/> |Segment de base 1 du chemin sur lequel calculer l’angle de la tangente. |

### <a name="return-value"></a>Valeur renvoyée

 **Double**
  
## <a name="remarks"></a>Remarques

Si vous ajoutez une valeur de *segment*, ANGLEALONGPATH renvoie la valeur de ce segment uniquement.
  
Si vous ajoutez une valeur de *segment*, ANGLEALONGPATH détermine le point de la tangente en utilisant *travel* pour calculer le pourcentage le long du *segment*.
  
Si *l’une* ou l’autre segment_ section n’existe pas, Microsoft Visio renvoie #REF!.
  