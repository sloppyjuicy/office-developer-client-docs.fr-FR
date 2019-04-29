---
title: ShapeRouteStyle, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm905
localization_priority: Normal
ms.assetid: a5dcd2e0-e343-5ee2-2b63-2a1312437901
description: Détermine le style et le sens de positionnement d'un connecteur sélectionné sur la page de dessin.
ms.openlocfilehash: e5725d461a71dad4623161d99134a20250abe724
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425028"
---
# <a name="shaperoutestyle-cell-shape-layout-section"></a>ShapeRouteStyle, cellule (section Shape Layout)

Détermine le style et le sens de positionnement d'un connecteur sélectionné sur la page de dessin.
  
|**Valeur**|**Style de positionnement**|**Direction**|**Constante d'automation**|
|:-----|:-----|:-----|:-----|
|0  <br/> |Utiliser valeur page par défaut  <br/> |Aucun  <br/> |**visLORouteDefault** <br/> |
|0,1  <br/> |Angle droit  <br/> |Aucun  <br/> |**visLORouteRightAngle** <br/> |
|n°2  <br/> |Tirant  <br/> |Aucun  <br/> |**visLORouteStraight** <br/> |
|3  <br/> |Organigramme  <br/> |De haut en bas  <br/> |**visLORouteOrgChartNS** <br/> |
|4  <br/> |Organigramme  <br/> |De gauche à droite  <br/> |**visLORouteOrgChartWE** <br/> |
|disque  <br/> |Diagramme de flux  <br/> |De haut en bas  <br/> |**visLORouteFlowchartNS** <br/> |
|6.x  <br/> |Diagramme de flux  <br/> |De gauche à droite  <br/> |**visLORouteFlowchartWE** <br/> |
|7j/7  <br/> |TreeView  <br/> |De haut en bas  <br/> |**visLORouteTreeNS** <br/> |
|8bits  <br/> |TreeView  <br/> |De gauche à droite  <br/> |**visLORouteTreeWE** <br/> |
|4,9  <br/> |Réseau  <br/> |Aucun  <br/> |**visLORouteNetwork** <br/> |
|10   <br/> |Organigramme  <br/> |De bas en haut  <br/> |**visLORouteOrgChartSN** <br/> |
|11   <br/> |Organigramme  <br/> |De droite à gauche  <br/> |**visLORouteOrgChartEW** <br/> |
|12   <br/> |Diagramme de flux  <br/> |De bas en haut  <br/> |**visLORouteFlowchartSN** <br/> |
|13   <br/> |Diagramme de flux  <br/> |De droite à gauche  <br/> |**visLORouteFlowchartEW** <br/> |
|14   <br/> |TreeView  <br/> |De bas en haut  <br/> |**visLORouteTreeSN** <br/> |
|15   <br/> |TreeView  <br/> |De droite à gauche  <br/> |**visLORouteTreeEW** <br/> |
|16   <br/> |Centre vers centre  <br/> |Aucun  <br/> |**visLORouteCenterToCenter** <br/> |
|17   <br/> |Simple  <br/> |De haut en bas  <br/> |**visLORouteSimpleNS** <br/> |
|18   <br/> |Simple  <br/> |De gauche à droite  <br/> |**visLORouteSimpleWE** <br/> |
|neuf  <br/> |Simple  <br/> |De bas en haut  <br/> |**visLORouteSimpleSN** <br/> |
|vingtaine  <br/> |Simple  <br/> |De droite à gauche  <br/> |**visLORouteSimpleEW** <br/> |
|21  <br/> |Horizontal-vertical simple  <br/> |Aucun  <br/> |**visLORouteSimpleHV** <br/> |
|22,5  <br/> |Vertical-horizontal simple  <br/> |Aucun  <br/> |**visLORouteSimpleVH** <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de cette cellule pour un connecteur particulier sous l'onglet **connecteur** dans la boîte de dialogue **comportement** (avec un connecteur sélectionné, cliquez sur **comportement** dans l'onglet [développeur](run-in-developer-mode-display-the-developer-tab.md) , puis cliquez sur l'onglet **connecteur** ). 
  
Pour définir ce comportement pour *tous* les connecteurs d'une page, utilisez la cellule RouteStyle de la section Page Layout. 
  
Dans les versions antérieures à Visio 2000, vous pouviez définir ce comportement en faisant appel à la cellule ObjBehavior de la section Miscellaneous.
  
Pour obtenir une référence à la cellule ShapeRouteStyle par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |ShapeRouteStyle  <br/> |
   
Pour obtenir une référence à la cellule ShapeRouteStyle à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**Définis** <br/> |
|Index de la ligne :  <br/> |**visRowShapeLayout** <br/> |
|Index de la cellule :  <br/> |**visSLORouteStyle** <br/> |
   

