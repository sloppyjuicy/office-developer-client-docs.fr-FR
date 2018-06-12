---
title: POINTALONGPATH, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7f91e5d9-89b8-5a0d-e01f-aa81fbd5e1fd
description: Renvoie les coordonnées d’un point du chemin, ou d’un décalage par rapport à ce chemin.
ms.openlocfilehash: 9ce6f8c171515b46aaff0ce07cbe7da4f1e958d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789267"
---
# <a name="pointalongpath-function"></a>POINTALONGPATH, fonction

Renvoie les coordonnées d’un point du chemin, ou d’un décalage par rapport à ce chemin.
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2010 
  
## <a name="syntax"></a>Syntaxe

POINTALONGPATH (** *section* **, ** *voyage* ** ** *[, décalage]* ** ** *[, segment]* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Section Geometry qui représente le chemin, spécifiée par une référence à sa cellule Path (par exemple Geometry1.Path).  <br/> |
| _frais de déplacement_ <br/> |Obligatoire  <br/> |**Double** <br/> |Pourcentage du chemin parcouru du point de début au point de fin qui identifie le point. La valeur doit être comprise entre 0 et 1.  <br/> |
| _décalage_ <br/> |Facultatif  <br/> |**Double** <br/> |Distance dont le point est décalé par rapport au chemin. Voir la section Remarques pour plus d’informations.  <br/> |
| _segment_ <br/> |Facultatif  <br/> |**Integer** <br/> |Segment de base 1 du chemin sur lequel calculer les coordonnées.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

 **Point**
  
## <a name="remarks"></a>Note

Si la _section_ ou _segment_ n’existe pas, Microsoft Visio renvoie #REF !. 
  
Les valeurs positives *décalage* spécifient des points vers la gauche de la direction de déplacement. 
  
Les valeurs négatives *décalage* spécifient des points à droite de la direction de déplacement. 
  
Un **Point** représente une paire classée de coordonnées géométriques (*x, y*) sous la forme d’une valeur unique. 
  

