---
title: RouteStyle, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251662
localization_priority: Normal
ms.assetid: 3a223dac-538b-cb5d-a32d-61395276f9da
description: Détermine le style et la direction du positionnement de tous les connecteurs de la page de dessin n'ayant pas de style de positionnement local.
ms.openlocfilehash: 38de871460c155ee5d495599a239ebeb0ff1c33d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424783"
---
# <a name="routestyle-cell-page-layout-section"></a>RouteStyle, cellule (section Page Layout)

Détermine le style et la direction du positionnement de tous les connecteurs de la page de dessin n'ayant pas de style de positionnement local.
  
|**Valeur**|**Style de positionnement**|**Direction**|**Constante d'automation**|
|:-----|:-----|:-----|:-----|
|0  <br/> |Valeur par défaut ; angle droit  <br/> |Aucun  <br/> |**visLORouteDefault** <br/> |
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

Vous pouvez également définir la valeur de cette cellule sous l'onglet **disposition et positionnement** de la boîte de dialogue mise en **page** (sous l'onglet **création** , cliquez sur la flèche **mise en page** , cliquez sur **disposition et positionnement**, puis cliquez sur **espacement** ). 
  
Vous pouvez définir le style de positionnement d'un connecteur dans la cellule ShapeRouteStyle de la section Shape Layout. 
  
Pour obtenir une référence à la cellule RouteStyle par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |RouteStyle  <br/> |
   
Pour obtenir une référence à la cellule RouteStyle à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**Définis** <br/> |
|Index de la ligne :  <br/> |**visRowPageLayout** <br/> |
|Index de la cellule :  <br/> |**visPLORouteStyle** <br/> |
   

