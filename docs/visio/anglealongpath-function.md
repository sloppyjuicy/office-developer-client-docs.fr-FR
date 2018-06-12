---
title: ANGLEALONGPATH, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d7f8ca9a-3a89-abab-9805-bd1e24075c3f
description: Renvoie l’angle de la tangente du chemin à un point donné.
ms.openlocfilehash: ec5529037275fc8661972cc7403886cd33150b38
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788043"
---
# <a name="anglealongpath-function"></a>ANGLEALONGPATH, fonction

Renvoie l’angle de la tangente du chemin à un point donné.
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2010 
  
## <a name="syntax"></a>Syntaxe

ANGLEALONGPATH (** *section* **, ** *voyage* ** ** *[, segment]* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Section Geometry qui représente le chemin, spécifiée par une référence à sa cellule Path (par exemple Geometry1.Path).  <br/> |
| _frais de déplacement_ <br/> |Obligatoire  <br/> |**Double** <br/> |Pourcentage le long du chemin du point de début au point de fin. La valeur doit être comprise entre 0 et 1.  <br/> |
| _segment_ <br/> |Facultatif  <br/> |**Integer** <br/> |Segment de base 1 du chemin sur lequel calculer l’angle de la tangente.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

 **Double**
  
## <a name="remarks"></a>Note

Si vous incluez une valeur de _segment_ , ANGLEALONGPATH renvoie la valeur de ce segment uniquement. 
  
Si vous incluez une valeur de _segment_ , ANGLEALONGPATH détermine le point de la tangente à l’aide de _déplacement_ pour calculer le pourcentage le long de _segment_du.
  
Si la _section_ ou _segment_ n’existe pas, Microsoft Visio renvoie #REF !. 
  

