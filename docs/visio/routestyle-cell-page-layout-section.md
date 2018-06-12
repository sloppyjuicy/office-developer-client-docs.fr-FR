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
ms.openlocfilehash: d64e7b3c7cf30f0a657ede57b227acefd4b10101
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789518"
---
# <a name="routestyle-cell-page-layout-section"></a>RouteStyle, cellule (section Page Layout)

Détermine le style et la direction du positionnement de tous les connecteurs de la page de dessin n'ayant pas de style de positionnement local.
  
|**Valeur**|**Style de positionnement**|**Direction**|**Constante d’Automation**|
|:-----|:-----|:-----|:-----|
|0  <br/> |Valeur par défaut ; angle droit  <br/> |Aucune  <br/> |**visLORouteDefault** <br/> |
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

Vous pouvez également définir la valeur de cette cellule sous l’onglet **disposition et positionnement** dans la boîte de dialogue **Mise en Page** (sous l’onglet **Création** , cliquez sur la flèche **Mise en Page** , cliquez sur **disposition et positionnement**, puis cliquez sur **espacement** ). 
  
Vous pouvez définir le style de positionnement d'un connecteur dans la cellule ShapeRouteStyle de la section Shape Layout. 
  
Pour obtenir une référence à la cellule RouteStyle par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |RouteStyle  <br/> |
   
Pour obtenir une référence à la cellule RouteStyle par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowPageLayout** <br/> |
|Index de la cellule :  <br/> |**visPLORouteStyle** <br/> |
   

