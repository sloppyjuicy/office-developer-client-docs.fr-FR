---
title: PATHLENGTH, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6f47ea08-fb5e-7d48-e84a-2a6570564924
description: Renvoie la longueur du chemin défini dans la section Geometry spécifiée.
ms.openlocfilehash: da00d0b144be5526eaa8d253b7b52a397af68538
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608068"
---
# <a name="pathlength-function"></a>Fonction PATHLENGTH

Renvoie la longueur du chemin défini dans la section Geometry spécifiée.
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2010
 
  
## <a name="syntax"></a>Syntaxe

PATHLENGTH(** *section* ** ** *[,segment]* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Obligatoire  <br/> |**String** <br/> |Section Geometry qui représente le chemin, spécifiée par une référence à sa cellule Path (par exemple Geometry1.Path).  <br/> |
| _segment_ <br/> |Facultatif  <br/> |**Integer** <br/> |Segment de base 1 du chemin à mesurer.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

 **Double**
  
## <a name="remarks"></a>Remarques

Si _section_ ou _segment_ n’existe pas, Microsoft Visio renvoie #REF!. 
  
Si vous incluez une valeur  _de segment,_ PATHLENGTH renvoie uniquement la longueur de ce segment. 
  

