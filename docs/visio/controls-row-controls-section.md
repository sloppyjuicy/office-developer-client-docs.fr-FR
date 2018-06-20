---
title: Controls, ligne (section Controls)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1024624
localization_priority: Normal
ms.assetid: a57bdcd9-566b-5054-7458-7d84cbb78d23
description: Contient les cellules qui définissent les coordonnées x - et y-coordonnées et le comportement de chaque poignée de contrôle définie pour une forme. Une forme contient une ligne Controls pour chaque poignée de contrôle.
ms.openlocfilehash: ed1d57fce6d413b9eb7f5d119264bc2bfa968222
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788363"
---
# <a name="controls-row-controls-section"></a>Controls, ligne (section Controls)

Contient les cellules qui définissent les coordonnées *x* - et *y* -coordonnées et le comportement de chaque poignée de contrôle définie pour une forme. Une forme contient une ligne Controls pour chaque poignée de contrôle. 
  
Les lignes Controls sont nommées Controls. *nom* et contiennent les cellules suivantes. Pour plus d’informations, consultez les rubriques de la cellule spécifique. 
  
|**Cell**|**Description**|
|:-----|:-----|
|[x](x-cell-controls-section.md) <br/> |Représente le *x* -coordonnées qui indique l’emplacement de la poignée de contrôle d’une forme dans le système de coordonnées local.  <br/> |
|[y](y-cell-controls-section.md) <br/> |Représente la valeur *y* -coordonnées qui indique l’emplacement de la poignée de contrôle d’une forme dans le système de coordonnées local.  <br/> |
|[X Dynamics](x-dynamics-cell-controls-section.md) <br/> |Représente le *x* -coordonnées d’un point d’ancrage d’une poignée de contrôle dans le système de coordonnées local.  <br/> |
|[Y Dynamics](y-dynamics-cell-controls-section.md) <br/> |Représente la valeur *y* -coordonnées d’un point d’ancrage d’une poignée de contrôle dans le système de coordonnées local.  <br/> |
|[X comportement](x-behavior-cell-controls-section.md) <br/> |Contrôle le type de comportement *x* -coordonnée de la poignée de contrôle se présentera après la poignée de déplacement.  <br/> |
|[Y Behavior](y-behavior-cell-controls-section.md) <br/> |Contrôle le type de comportement *y* -coordonnée de la poignée de contrôle se présentera après la poignée de déplacement.  <br/> |
|[Can Glue](can-glue-cell-controls-section.md) <br/> |Détermine si une poignée de contrôle peut être collée à d'autres formes.  <br/> |
|[Info-bulle](tip-cell-controls-section.md) <br/> |Représente une chaîne de texte descriptive qui apparaît sous la forme d'une info-bulle lorsqu'un utilisateur maintient quelques instants le pointeur sur la poignée de contrôle d'une forme.  <br/> |
   
## <a name="remarks"></a>Notes

 Vous pouvez ajouter autant de contrôles.  *nom de* lignes que vous le souhaitez, assigner des noms explicites aux lignes et définir des valeurs de cellule. Pour ajouter des poignées de contrôle à une section Controls existante, cliquez sur une ligne, cliquez sur **Insérer une ligne** dans le menu contextuel. 
  
Vous pouvez référencer ces cellules par leur nom de ligne, qui s’affiche dans une fenêtre feuille ShapeSheet en texte rouge. Pour attribuer des noms explicites à des contrôles. *nom de* lignes, cliquez sur la ligne, puis tapez *personnalisé* , par exemple, pour créer le nom de ligne Controls.personnalisée. Vous pouvez ensuite référencer la cellule X à l’aide de Controls.personnalisée.x. 
  
Le nom de ligne que vous entrez doit être unique dans la section.
  

