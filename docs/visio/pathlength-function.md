---
title: PATHLENGTH, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6f47ea08-fb5e-7d48-e84a-2a6570564924
description: Renvoie la longueur du chemin défini dans la section Geometry spécifiée.
ms.openlocfilehash: 9efac03ab478c86e250abb4d1c7893ec2f955d7d
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63405587"
---
# <a name="pathlength-function"></a>Fonction PATHLENGTH

Renvoie la longueur du chemin défini dans la section Geometry spécifiée.
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2010

  
## <a name="syntax"></a>Syntaxe

PATHLENGTH(***section** _ _*_[,segment]_** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *section* <br/> |Requis  <br/> |**String** <br/> |Section Geometry qui représente le chemin, spécifiée par une référence à sa cellule Path (par exemple Geometry1.Path). |
| *segment* <br/> |Facultatif  <br/> |**Integer** <br/> |Segment de base 1 du chemin à mesurer. |

### <a name="return-value"></a>Valeur renvoyée

 **Double**
  
## <a name="remarks"></a>Remarques

Si l’argument *section* ou *segment* n’existe pas, Microsoft Visio renvoie #REF!.
  
Si vous ajoutez une valeur de *segment*, PATHLENGTH renvoie la longueur de ce segment uniquement.
