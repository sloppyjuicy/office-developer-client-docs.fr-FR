---
title: ShapeRouteStyle, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm905
ms.localizationpriority: medium
ms.assetid: a5dcd2e0-e343-5ee2-2b63-2a1312437901
description: Détermine le style et le sens de positionnement d'un connecteur sélectionné sur la page de dessin.
ms.openlocfilehash: c578b7ba1564b18b9f8569037bc94ab63bbcb6b6
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63521735"
---
# <a name="shaperoutestyle-cell-shape-layout-section"></a>ShapeRouteStyle, cellule (section Shape Layout)

Détermine le style et le sens de positionnement d'un connecteur sélectionné sur la page de dessin.
  
|**Valeur**|**Style de positionnement**|**Direction**|**Constante d'automation**|
|:-----|:-----|:-----|:-----|
|0  <br/> |Utiliser valeur page par défaut  <br/> |Aucun  <br/> |**visLORouteDefault** <br/> |
|1  <br/> |Angle droit  <br/> |Aucune  <br/> |**visLORouteRightAngle** <br/> |
|2  <br/> |Droite  <br/> |Aucune  <br/> |**visLORouteStraight** <br/> |
|3  <br/> |Organigramme  <br/> |De haut en bas  <br/> |**visLORouteOrgChartNS** <br/> |
|4  <br/> |Organigramme  <br/> |De gauche à droite  <br/> |**visLORouteOrgChartWE** <br/> |
|5  <br/> |Diagramme de flux  <br/> |De haut en bas  <br/> |**visLORouteFlowchartNS** <br/> |
|6   <br/> |Diagramme de flux  <br/> |De gauche à droite  <br/> |**visLORouteFlowchartWE** <br/> |
|7   <br/> |Arborescence  <br/> |De haut en bas  <br/> |**visLORouteTreeNS** <br/> |
|8   <br/> |Arborescence  <br/> |De gauche à droite  <br/> |**visLORouteTreeWE** <br/> |
|9   <br/> |Réseau  <br/> |Aucun  <br/> |**visLORouteNetwork** <br/> |
|10  <br/> |Organigramme  <br/> |De bas en haut  <br/> |**visLORouteOrgChartSN** <br/> |
|11  <br/> |Organigramme  <br/> |De droite à gauche  <br/> |**visLORouteOrgChartEW** <br/> |
|12   <br/> |Diagramme de flux  <br/> |De bas en haut  <br/> |**visLORouteFlowchartSN** <br/> |
|13  <br/> |Diagramme de flux  <br/> |De droite à gauche  <br/> |**visLORouteFlowchartEW** <br/> |
|14   <br/> |Arborescence  <br/> |De bas en haut  <br/> |**visLORouteTreeSN** <br/> |
|15   <br/> |Arborescence  <br/> |De droite à gauche  <br/> |**visLORouteTreeEW** <br/> |
|16  <br/> |Centre vers centre  <br/> |Aucune  <br/> |**visLORouteCenterToCenter** <br/> |
|17   <br/> |Simple  <br/> |De haut en bas  <br/> |**visLORouteSimpleNS** <br/> |
|18   <br/> |Simple  <br/> |De gauche à droite  <br/> |**visLORouteSimpleWE** <br/> |
|19  <br/> |Simple  <br/> |De bas en haut  <br/> |**visLORouteSimpleSN** <br/> |
|20  <br/> |Simple  <br/> |De droite à gauche  <br/> |**visLORouteSimpleEW** <br/> |
| 21  <br/> |Horizontal-vertical simple  <br/> |Aucune  <br/> |**visLORouteSimpleHV** <br/> |
|22  <br/> |Vertical-horizontal simple  <br/> |Aucun  <br/> |**visLORouteSimpleVH** <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de cette cellule pour un connecteur particulier sous l’onglet Connecteur dans la boîte de dialogue Comportement (avec un connecteur sélectionné, cliquez sur Comportement [](run-in-developer-mode-display-the-developer-tab.md) sous l’onglet Développeur, puis  cliquez sur l’onglet Connecteur).   
  
Pour définir ce comportement pour  *tous les connecteurs*  d’une page, utilisez la cellule RouteStyle dans la section Mise en page. 
  
Dans les versions antérieures à Visio 2000, vous pouviez définir ce comportement en faisant appel à la cellule ObjBehavior de la section Miscellaneous.
  
Pour obtenir une référence à la cellule ShapeRouteStyle par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de la cellule :**  <br/> |ShapeRouteStyle  <br/> |
   
Pour obtenir une référence à la cellule ShapeRouteStyle à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRowShapeLayout** <br/> |
|**Index de la cellule :**  <br/> |**visSLORouteStyle** <br/> |
   

