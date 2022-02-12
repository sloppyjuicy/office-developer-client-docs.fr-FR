---
title: POINTALONGPATH, fonction
manager: lindalu
ms.date: 02/09/2022
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 7f91e5d9-89b8-5a0d-e01f-aa81fbd5e1fd
description: Renvoie les coordonnées d’un point du chemin, ou d’un décalage par rapport à ce chemin.
ms.openlocfilehash: 29ec31e6600f7ecdfd7c22bff0e05c113cb06fc5
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62777116"
---
# <a name="pointalongpath-function"></a>Fonction POINTALONGPATH

Renvoie les coordonnées d’un point du chemin, ou d’un décalage par rapport à ce chemin.
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2010

  
## <a name="syntax"></a>Syntaxe

POINTALONGPATH(***section**_, _*_travel_*_ _*_[,offset]_*_ _*_[,segment]_** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *section* |Requis |**String** |Section Geometry qui représente le chemin, spécifiée par une référence à sa cellule Path (par exemple Geometry1.Path). |
| *travel* |Obligatoire |**Double** |Pourcentage du chemin parcouru du point de début au point de fin qui identifie le point. La valeur doit être comprise entre 0 et 1. |
| *offset* |Facultatif |**Double** |Distance dont le point est décalé par rapport au chemin. Voir la section Remarques pour plus d’informations. |
| *segment* |Facultatif |**Integer** |Segment de base 1 du chemin sur lequel calculer les coordonnées. |

### <a name="return-value"></a>Valeur renvoyée

**Point**
  
## <a name="remarks"></a>Remarques

Si l’argument *section* ou *segment* n’existe pas, Microsoft Visio renvoie #REF!.
  
Les  *valeurs de*  décalage positif spécifient des points à gauche de la direction du déplacement.
  
Les  *valeurs de*  décalage négatives spécifient des points à droite de la direction du déplacement.
  
Un **Point** représente une paire classée de coordonnées géométriques (*x,y*) sous forme de valeur unique.
