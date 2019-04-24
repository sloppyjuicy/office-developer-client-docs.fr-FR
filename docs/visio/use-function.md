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
description: Applique le motif de trait, le motif de remplissage ou l'extrémité de trait appelé nom à la forme lorsqu'elle est placée dans la cellule LinePattern, FillPattern, BeginArrow ou EndArrow.
ms.openlocfilehash: ddd15c1c127fafa1a230545d544c74956f5c0262
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337148"
---
# <a name="use-function"></a>Fonction USE

Applique le motif de trait, le motif de remplissage ou l'extrémité de trait appelé _nom_ à la forme lorsqu'elle est placée dans la cellule LinePattern, FillPattern, BeginArrow ou EndArrow. 
  
## <a name="syntax"></a>Syntaxe

USE ("* * *Name* * *") 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _nom_ <br/> |Obligatoire  <br/> |**String** <br/> |Chaîne correspondant à un nom de forme de base valide.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Nombre
  
## <a name="remarks"></a>Remarques

Si une forme de base nommée _nom_ est présente sur le gabarit de document du document, le motif est appliqué en tant que motif de trait, motif de remplissage, flèche de début ou flèche de fin. 
  
Cette fonction renvoie toujours 254.
  
## <a name="example"></a>Exemple

USE("Voies ferrées") 
  
Formate la forme en appliquant le motif de base intitulé Voies ferrées à la forme contenant la formule. 
  

