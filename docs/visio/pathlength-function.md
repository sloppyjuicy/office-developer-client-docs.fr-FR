---
title: PATHLENGTH, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f47ea08-fb5e-7d48-e84a-2a6570564924
description: Renvoie la longueur du chemin défini dans la section Geometry spécifiée.
ms.openlocfilehash: 37cabbde9fc0782bc1fde46f3065d0c945c9dada
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789227"
---
# <a name="pathlength-function"></a>PATHLENGTH, fonction

Renvoie la longueur du chemin défini dans la section Geometry spécifiée.
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2010 
  
## <a name="syntax"></a>Syntaxe

PATHLENGTH (** *section* ** ** *[, segment]* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Section Geometry qui représente le chemin, spécifiée par une référence à sa cellule Path (par exemple Geometry1.Path).  <br/> |
| _segment_ <br/> |Facultatif  <br/> |**Integer** <br/> |Segment de base 1 du chemin à mesurer.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

 **Double**
  
## <a name="remarks"></a>Note

Si la _section_ ou _segment_ n’existe pas, Microsoft Visio renvoie #REF !. 
  
Si vous incluez une valeur de _segment_ , PATHLENGTH renvoie la longueur de ce segment uniquement. 
  

