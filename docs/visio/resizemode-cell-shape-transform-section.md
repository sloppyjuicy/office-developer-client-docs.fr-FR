---
title: ResizeMode, cellule (section Shape Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251203
localization_priority: Normal
ms.assetid: 49816e46-fa83-3ee4-1451-9c85fbd0f519
description: Indique le mode de redimensionnement actuel pour la forme.
ms.openlocfilehash: 7e9080fcd4604e2dbdc1dae31992f05e5b512213
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326879"
---
# <a name="resizemode-cell-shape-transform-section"></a>ResizeMode, cellule (section Shape Transform)

Indique le mode de redimensionnement actuel pour la forme.
  
|**Value**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
|0  <br/> |Utiliser les paramètres du groupe  <br/> |**visXFormResizeDontCare** <br/> |
|0,1  <br/> |Repositionner seulement  <br/> |**visXFormResizeSpread** <br/> |
|n°2  <br/> |Mettre à l'échelle avec le groupe  <br/> |**visXFormResizeScale** <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir cette valeur sous l'onglet **comportement** dans la boîte de dialogue **comportement** (sous l'onglet [développeur](run-in-developer-mode-display-the-developer-tab.md), dans le groupe **création de forme** , cliquez sur **comportement**). Pour obtenir une référence à la cellule ResizeMode par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |ResizeMode  <br/> |
   
Pour obtenir une référence à la cellule ResizeMode à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**Définis** <br/> |
|Index de la ligne :  <br/> |**visRowXFormOut** <br/> |
|Index de la cellule :  <br/> |**visXFormResizeMode** <br/> |
   

