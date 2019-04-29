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
description: Contient les cellules qui définissent les coordonnées x et y et le comportement de chaque poignée de contrôle définie pour une forme. Une forme contient une ligne contrôles pour chaque poignée de contrôle.
ms.openlocfilehash: dd5a96fe297cb62996ac2ab4d2974b8d1ae61a14
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438189"
---
# <a name="controls-row-controls-section"></a>Controls Row (Controls Section)

Contient les cellules qui définissent les coordonnées *x* et *y* et le comportement de chaque poignée de contrôle définie pour une forme. Une forme contient une ligne contrôles pour chaque poignée de contrôle. 
  
Les lignes Controls sont nommées Controls. *nom* et contient les cellules suivantes. Pour plus de détails, consultez les rubriques spécifiques aux cellules. 
  
|**Cellule**|**Description**|
|:-----|:-----|
|[x](x-cell-controls-section.md) <br/> |Représente la coordonnée *x* qui indique l'emplacement de la poignée de contrôle d'une forme en coordonnées locales.  <br/> |
|[y](y-cell-controls-section.md) <br/> |Représente la coordonnée *y* qui indique l'emplacement de la poignée de contrôle d'une forme en coordonnées locales.  <br/> |
|[X Dynamics](x-dynamics-cell-controls-section.md) <br/> |Représente la coordonnée *x* du point d'ancrage d'une poignée de contrôle, exprimée dans le système de coordonnées locales.  <br/> |
|[Y Dynamics](y-dynamics-cell-controls-section.md) <br/> |Représente la coordonnée *y* du point d'ancrage d'une poignée de contrôle, exprimée dans le système de coordonnées locales.  <br/> |
|[X Behavior](x-behavior-cell-controls-section.md) <br/> |Contrôle le type de comportement de la coordonnée *x* de la poignée de contrôle une fois que celle-ci a été déplacée.  <br/> |
|[Y Behavior](y-behavior-cell-controls-section.md) <br/> |Contrôle le type de comportement de la coordonnée *y* de la poignée de contrôle une fois que cette dernière a été déplacée.  <br/> |
|[Can Glue](can-glue-cell-controls-section.md) <br/> |Détermine si une poignée de contrôle peut être collée à d'autres formes.  <br/> |
|[TETE](tip-cell-controls-section.md) <br/> |Représente une chaîne de texte descriptive qui apparaît sous la forme d'une info-bulle lorsqu'un utilisateur maintient quelques instants le pointeur sur la poignée de contrôle d'une forme.  <br/> |
   
## <a name="remarks"></a>Remarques

 Vous pouvez ajouter autant de lignes Controls.  *Nommez* les lignes selon vos besoins, assignez des noms parlants aux lignes et définissez des valeurs de cellule. Pour ajouter des poignées de contrôle à une section Controls existante, cliquez avec le bouton droit de la souris, puis cliquez sur **Insérer une ligne** dans le menu contextuel. 
  
Vous pouvez désigner ces cellules à l'aide de leur nom de ligne, qui apparaît en rouge dans la fenêtre Feuille ShapeSheet. Pour assigner des noms parlants aux lignes Controls. *Nommez* des lignes, cliquez sur la ligne, puis tapez *Custom* , par exemple, pour créer le nom de ligne Controls. Custom. Vous pouvez alors faire référence à la cellule X en utilisant Controls.Personnalisée.X. 
  
Le nom de ligne que vous entrez doit être unique dans la section.
  

