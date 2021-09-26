---
title: POINTALONGPATH, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 7f91e5d9-89b8-5a0d-e01f-aa81fbd5e1fd
description: Renvoie les coordonnées d’un point du chemin, ou d’un décalage par rapport à ce chemin.
ms.openlocfilehash: b436378ee874c3ecf3fc51d07ac80f461c6cfa3c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598422"
---
# <a name="pointalongpath-function"></a>Fonction POINTALONGPATH

Renvoie les coordonnées d’un point du chemin, ou d’un décalage par rapport à ce chemin.
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2010
 
  
## <a name="syntax"></a>Syntaxe

POINTALONGPATH(** *section* **, ** *travel* ** ** *[,offset]* ** ** *[,segment]* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Obligatoire  <br/> |**String** <br/> |Section Geometry qui représente le chemin, spécifiée par une référence à sa cellule Path (par exemple Geometry1.Path).  <br/> |
| _travel_ <br/> |Obligatoire  <br/> |**Double** <br/> |Pourcentage du chemin parcouru du point de début au point de fin qui identifie le point. La valeur doit être comprise entre 0 et 1.  <br/> |
| _offset_ <br/> |Facultatif  <br/> |**Double** <br/> |Distance dont le point est décalé par rapport au chemin. Voir la section Remarques pour plus d’informations.  <br/> |
| _segment_ <br/> |Facultatif  <br/> |**Integer** <br/> |Segment de base 1 du chemin sur lequel calculer les coordonnées.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

 **Point**
  
## <a name="remarks"></a>Remarques

Si _section_ ou _segment_ n’existe pas, Microsoft Visio renvoie #REF!. 
  
Les  *valeurs de*  décalage positif spécifient des points à gauche du sens de déplacement. 
  
Les  *valeurs de*  décalage négatives spécifient des points à droite de la direction du déplacement. 
  
Un **Point** représente une paire classée de coordonnées géométriques (*x,y*) sous forme de valeur unique. 
  

