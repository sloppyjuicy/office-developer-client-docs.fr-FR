---
title: ANGLEALONGPATH, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d7f8ca9a-3a89-abab-9805-bd1e24075c3f
description: Renvoie l’angle de la tangente du chemin à un point donné.
ms.openlocfilehash: 0d38fc0e123a7e38b7826b55415cfc09c1789c0e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341418"
---
# <a name="anglealongpath-function"></a>Fonction ANGLEALONGPATH

Renvoie l’angle de la tangente du chemin à un point donné.
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2010
 
  
## <a name="syntax"></a>Syntaxe

ANGLEALONGPATH (* * *section* * *, * * *voyages* * * * * *[, segment]* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Obligatoire  <br/> |**String** <br/> |Section Geometry qui représente le chemin, spécifiée par une référence à sa cellule Path (par exemple Geometry1.Path).  <br/> |
| _poche_ <br/> |Obligatoire  <br/> |**Double** <br/> |Pourcentage le long du chemin du point de début au point de fin. La valeur doit être comprise entre 0 et 1.  <br/> |
| _segment_ <br/> |Facultatif  <br/> |**Integer** <br/> |Segment de base 1 du chemin sur lequel calculer l’angle de la tangente.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

 **Double**
  
## <a name="remarks"></a>Remarques

Si vous incluez une valeur de _segment_ , ANGLEALONGPATH renvoie la valeur de ce segment uniquement. 
  
Si vous incluez une valeur de _segment_ , ANGLEALONGPATH détermine le point de la tangente à l'aide de _voyages_ pour calculer le pourcentage de percertification le long du _segment_.
  
Si l'une des _sections_ ou le _segment_ n'existe pas, Microsoft Visio renvoie #REF!. 
  

