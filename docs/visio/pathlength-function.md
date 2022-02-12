---
title: PATHLENGTH, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6f47ea08-fb5e-7d48-e84a-2a6570564924
description: Renvoie la longueur du chemin défini dans la section Geometry spécifiée.
ms.openlocfilehash: 02c269dae2dfa89567da5274e31d64df0395a508
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62788821"
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
| _section_ <br/> |Requis  <br/> |**String** <br/> |Section Geometry qui représente le chemin, spécifiée par une référence à sa cellule Path (par exemple Geometry1.Path). |
| _segment_ <br/> |Facultatif  <br/> |**Integer** <br/> |Segment de base 1 du chemin à mesurer. |

### <a name="return-value"></a>Valeur renvoyée

 **Double**
  
## <a name="remarks"></a>Remarques

Si l’argument _section_ ou _segment_ n’existe pas, Microsoft Visio renvoie #REF!.
  
Si vous ajoutez une valeur de _segment_, PATHLENGTH renvoie la longueur de ce segment uniquement.