---
title: PlowCode, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251660
localization_priority: Normal
ms.assetid: e43f3d29-7def-d36e-ac64-62f0a389d415
description: Détermine si les formes positionnables se déplacent lorsque vous déposez une forme positionnable à côté d'une autre forme positionnable sur une page de dessin.
ms.openlocfilehash: e180ce679f280cbccbda80b67170f2f26473bd8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789273"
---
# <a name="plowcode-cell-page-layout-section"></a>PlowCode, cellule (section Page Layout)

Détermine si les formes positionnables se déplacent lorsque vous déposez une forme positionnable à côté d'une autre forme positionnable sur une page de dessin.
  
|**Valeur**|**Description**|**Constante d’Automation**|
|:-----|:-----|:-----|
|0  <br/> |Ne pas déplacer les formes  <br/> |**visPLOPlowNone** <br/> |
|1  <br/> |Déplacer les formes  <br/> |**visPLOPlowAll** <br/> |
   
## <a name="remarks"></a>Note

Vous pouvez également définir la valeur de cette cellule sous l’onglet **disposition et positionnement** dans la boîte de dialogue **Mise en Page** (sous l’onglet **Création** , cliquez sur la flèche **Mise en Page** ) à l’aide de la case à cocher **déplacer les autres formes lors de l’insertion** . 
  
Pour obtenir une référence à la cellule PlowCode par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |PlowCode  <br/> |
   
Pour obtenir une référence à la cellule PlowCode par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowPageLayout** <br/> |
|Index de la cellule :  <br/> |**visPLOPlowCode** <br/> |
   

