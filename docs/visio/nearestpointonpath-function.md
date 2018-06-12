---
title: NEARESTPOINTONPATH, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 539bf79a-df09-2048-2aba-8c863dd26fc2
description: Renvoie le pourcentage de la distance le long du chemin du point le plus proche des coordonnées spécifiées, sous la forme d’une valeur comprise entre 0 et 1.
ms.openlocfilehash: d9e9b890033526fec99f04cee30ae93578487652
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789158"
---
# <a name="nearestpointonpath-function"></a>NEARESTPOINTONPATH, fonction

Renvoie le pourcentage de la distance le long du chemin du point le plus proche des coordonnées spécifiées, sous la forme d’une valeur comprise entre 0 et 1.
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2010 
  
## <a name="syntax"></a>Syntaxe

NEARESTPOINTONPATH (** *section* **, ** *x* **, ** *y* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Section Geometry qui représente le chemin, spécifiée par une référence à sa cellule Path (par exemple Geometry1.Path).  <br/> |
| _x_ <br/> |Obligatoire  <br/> |**Double** <br/> |_X_-coordonnées du point spécifié.  <br/> |
| _y_ <br/> |Obligatoire  <br/> |**Double** <br/> |La valeur _y_-coordonnées du point spécifié.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

 **Double**
  
## <a name="remarks"></a>Note

Si la _section_ n’existe pas, Microsoft Visio renvoie #REF !. 
  

