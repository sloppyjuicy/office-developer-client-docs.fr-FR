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
description: Applique le nom appelé motif de trait, motif de remplissage ou fin de trait à la forme lorsqu’il est placé dans la cellule LinePattern, FillPattern, BeginArrow ou EndArrow.
ms.openlocfilehash: ddd15c1c127fafa1a230545d544c74956f5c0262
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422823"
---
# <a name="use-function"></a>Fonction USE

Applique le nom appelé motif de  trait, motif de remplissage ou fin de trait à la forme lorsqu’il est placé dans la cellule LinePattern, FillPattern, BeginArrow ou EndArrow. 
  
## <a name="syntax"></a>Syntaxe

USE( » ** *name* ** « ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _nom_ <br/> |Obligatoire  <br/> |**String** <br/> |Chaîne correspondant à un nom de forme de base valide.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Nombre
  
## <a name="remarks"></a>Remarques

Si un  nom nommé de forme de fond est présent dans le gabarit du document, le motif est appliqué en tant que motif de trait, motif de remplissage, flèche de début ou flèche de fin. 
  
Cette fonction renvoie toujours 254.
  
## <a name="example"></a>Exemple

USE("Voies ferrées") 
  
Formate la forme en appliquant le motif de base intitulé Voies ferrées à la forme contenant la formule. 
  

