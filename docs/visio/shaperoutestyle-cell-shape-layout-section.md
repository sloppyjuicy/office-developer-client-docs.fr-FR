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
ms.openlocfilehash: b165d43e64842565806d93d620ddbd24f41a2d57
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789656"
---
# <a name="shaperoutestyle-cell-shape-layout-section"></a>ShapeRouteStyle, cellule (section Shape Layout)

Détermine le style et le sens de positionnement d'un connecteur sélectionné sur la page de dessin.
  
|**Valeur**|**Style de positionnement**|**Direction**|**Constante d’Automation**|
|:-----|:-----|:-----|:-----|
|0  <br/> |Utiliser valeur page par défaut  <br/> |Aucun  <br/> |**visLORouteDefault** <br/> |
|1  <br/> |Angle droit  <br/> |Aucune  <br/> |**visLORouteRightAngle** <br/> |
|2  <br/> |Droit  <br/> |Aucune  <br/> |**visLORouteStraight** <br/> |
|3  <br/> |Organigramme  <br/> |De haut en bas  <br/> |**visLORouteOrgChartNS** <br/> |
|4  <br/> |Organigramme  <br/> |De gauche à droite  <br/> |**visLORouteOrgChartWE** <br/> |
|5  <br/> |Diagramme de flux  <br/> |De haut en bas  <br/> |**visLORouteFlowchartNS** <br/> |
|6  <br/> |Diagramme de flux  <br/> |De gauche à droite  <br/> |**visLORouteFlowchartWE** <br/> |
|7  <br/> |Arbre  <br/> |De haut en bas  <br/> |**visLORouteTreeNS** <br/> |
|8  <br/> |Arbre  <br/> |De gauche à droite  <br/> |**visLORouteTreeWE** <br/> |
|9  <br/> |Réseau  <br/> |Aucune  <br/> |**visLORouteNetwork** <br/> |
|10  <br/> |Organigramme  <br/> |De bas en haut  <br/> |**visLORouteOrgChartSN** <br/> |
|11  <br/> |Organigramme  <br/> |De droite à gauche  <br/> |**visLORouteOrgChartEW** <br/> |
|12  <br/> |Diagramme de flux  <br/> |De bas en haut  <br/> |**visLORouteFlowchartSN** <br/> |
|13  <br/> |Diagramme de flux  <br/> |De droite à gauche  <br/> |**visLORouteFlowchartEW** <br/> |
|14  <br/> |Arbre  <br/> |De bas en haut  <br/> |**visLORouteTreeSN** <br/> |
|15  <br/> |Arbre  <br/> |De droite à gauche  <br/> |**visLORouteTreeEW** <br/> |
|16  <br/> |Centre vers centre  <br/> |Aucune  <br/> |**visLORouteCenterToCenter** <br/> |
|17  <br/> |Simple  <br/> |De haut en bas  <br/> |**visLORouteSimpleNS** <br/> |
|18  <br/> |Simple  <br/> |De gauche à droite  <br/> |**visLORouteSimpleWE** <br/> |
|19  <br/> |Simple  <br/> |De bas en haut  <br/> |**visLORouteSimpleSN** <br/> |
|20  <br/> |Simple  <br/> |De droite à gauche  <br/> |**visLORouteSimpleEW** <br/> |
|21  <br/> |Horizontal-vertical simple  <br/> |Aucune  <br/> |**visLORouteSimpleHV** <br/> |
|22  <br/> |Vertical-horizontal simple  <br/> |Aucune  <br/> |**visLORouteSimpleVH** <br/> |
   
## <a name="remarks"></a>Note

Vous pouvez également définir la valeur de cette cellule pour un connecteur donné dans l’onglet **connecteur** dans la boîte de dialogue **comportement** (avec un connecteur sélectionné, cliquez sur **comportement** sous l’onglet [développeur](run-in-developer-mode-display-the-developer-tab.md) , puis cliquez sur l’onglet **connecteur** ). 
  
Pour définir ce comportement pour *toutes* les connecteurs sur une page, utilisez la cellule RouteStyle de la section Page Layout. 
  
Dans les versions antérieures à Visio 2000, vous pouviez définir ce comportement en faisant appel à la cellule ObjBehavior de la section Miscellaneous.
  
Pour obtenir une référence à la cellule ShapeRouteStyle par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |ShapeRouteStyle  <br/> |
   
Pour obtenir une référence à la cellule ShapeRouteStyle par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowShapeLayout** <br/> |
|Index de la cellule :  <br/> |**visSLORouteStyle** <br/> |
   

