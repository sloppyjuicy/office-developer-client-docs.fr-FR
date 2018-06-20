---
title: USE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251510
localization_priority: Normal
ms.assetid: 410c4187-21f3-d959-750e-9dc6095fba9a
description: Applique le motif de trait, motif de remplissage ou extrémité de trait appelé nom à la forme lorsqu’il est placé dans la cellule LinePattern, FillPattern, BeginArrow ou EndArrow.
ms.openlocfilehash: 0b6668e57a8f997a69fece51cbc5bd1b1574a576
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789978"
---
# <a name="use-function"></a>USE, fonction

Applique le motif de trait, motif de remplissage ou extrémité de trait appelé _nom_ à la forme lorsqu’il est placé dans la cellule LinePattern, FillPattern, BeginArrow ou EndArrow. 
  
## <a name="syntax"></a>Syntaxe

UTILISATION (« ** *nom* ** ») 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _nom_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Chaîne correspondant à un nom de forme de base valide.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Nombre
  
## <a name="remarks"></a>Remarques

Si une forme de base appelée _nom_ est présent dans le gabarit de document du document, le motif est appliqué comme un motif de trait, motif de remplissage, flèche de départ ou flèche de fin. 
  
Cette fonction renvoie toujours 254.
  
## <a name="example"></a>Exemple

USE("Voies ferrées") 
  
Formate la forme en appliquant le motif de base intitulé Voies ferrées à la forme contenant la formule. 
  

