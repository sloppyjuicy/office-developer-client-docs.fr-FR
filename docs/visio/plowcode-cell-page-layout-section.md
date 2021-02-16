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
ms.openlocfilehash: 4ea85ddbaf7662305a2a82fc7f0b814019624841
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420352"
---
# <a name="plowcode-cell-page-layout-section"></a>PlowCode, cellule (section Page Layout)

Détermine si les formes positionnables se déplacent lorsque vous déposez une forme positionnable à côté d'une autre forme positionnable sur une page de dessin.
  
|**Valeur**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
|0  <br/> |Ne pas déplacer les formes  <br/> |**visPLOPlowNone** <br/> |
|1   <br/> |Déplacer les formes  <br/> |**visPLOPlowAll** <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur  de cette cellule sous l’onglet Mise en page et routage dans  la boîte de dialogue Mise en **page** (sous l’onglet Création, cliquez sur la flèche Mise en **page)** à l’aide de la case à cocher Déplacer d’autres formes dans la zone de dépôt.  
  
Pour obtenir une référence à la cellule PlowCode par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |PlowCode  <br/> |
   
Pour obtenir une référence à la cellule PlowCode à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowPageLayout** <br/> |
|Index de la cellule :  <br/> |**visPLOPlowCode** <br/> |
   

