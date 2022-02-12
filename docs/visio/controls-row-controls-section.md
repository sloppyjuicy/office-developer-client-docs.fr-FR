---
title: Controls, ligne (section Controls)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1024624
ms.localizationpriority: medium
ms.assetid: a57bdcd9-566b-5054-7458-7d84cbb78d23
description: Contient les cellules qui définissent les coordonnées x et y et le comportement de chaque poignée de contrôle définie pour une forme. Une forme contient une ligne Controls pour chaque poignée de contrôle.
ms.openlocfilehash: 856a7204113f76cd5944df1c45414d0161248168
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62788919"
---
# <a name="controls-row-controls-section"></a>Controls Row (Controls Section)

Contient les cellules qui définissent les  *coordonnées x*  et  *y*  et le comportement de chaque poignée de contrôle définie pour une forme. Une forme contient une ligne Controls pour chaque poignée de contrôle. 
  
Les lignes Controls sont nommées Controls. *et*  contiennent les cellules suivantes. Pour plus de détails, consultez les rubriques spécifiques aux cellules. 
  
|**Cell**|**Description**|
|:-----|:-----|
|[x](x-cell-controls-section.md) <br/> |Représente la coordonnée  *x*  qui indique l’emplacement de la poignée de contrôle d’une forme dans les coordonnées locales. |
|[y](y-cell-controls-section.md) <br/> |Représente la coordonnée  *y*  qui indique l’emplacement de la poignée de contrôle d’une forme dans les coordonnées locales. |
|[X Dynamics](x-dynamics-cell-controls-section.md) <br/> |Représente la coordonnée  *x*  du point d’ancrage d’une poignée de contrôle dans les coordonnées locales. |
|[Y Dynamics](y-dynamics-cell-controls-section.md) <br/> |Représente la coordonnée  *y*  du point d’ancrage d’une poignée de contrôle dans les coordonnées locales. |
|[X Behavior](x-behavior-cell-controls-section.md) <br/> |Contrôle le type de comportement de la  *coordonnée x*  de la poignée de contrôle une fois la poignée déplacée. |
|[Y Behavior](y-behavior-cell-controls-section.md) <br/> |Contrôle le type de comportement de la coordonnée  *y*  de la poignée de contrôle une fois le handle déplacé. |
|[Can Glue](can-glue-cell-controls-section.md) <br/> |Détermine si une poignée de contrôle peut être collée à d'autres formes. |
|[Conseil](tip-cell-controls-section.md) <br/> |Représente une chaîne de texte descriptive qui apparaît sous la forme d'une info-bulle lorsqu'un utilisateur maintient quelques instants le pointeur sur la poignée de contrôle d'une forme. |
   
## <a name="remarks"></a>Remarques

 Vous pouvez ajouter autant de lignes Controls.  *nommez*  les lignes selon vos besoins, attribuez des noms significatifs aux lignes et définissez des valeurs de cellule. Pour ajouter des poignées de contrôle à une section Controls existante, cliquez avec le bouton droit de la souris, puis cliquez sur **Insérer une ligne** dans le menu contextuel. 
  
Vous pouvez désigner ces cellules à l'aide de leur nom de ligne, qui apparaît en rouge dans la fenêtre Feuille ShapeSheet. Pour assigner des noms parlants aux lignes Controls. *name*  rows, click the row and then type  *Custom*  , for example, to create the row name Controls.Custom. Vous pouvez alors faire référence à la cellule X en utilisant Controls.Personnalisée.X. 
  
Le nom de ligne que vous entrez doit être unique dans la section.
  

