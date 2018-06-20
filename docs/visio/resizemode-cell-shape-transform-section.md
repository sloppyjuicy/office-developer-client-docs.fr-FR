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
ms.openlocfilehash: a32f5dbc935e85a49ab585073ca6a31215fd102a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789507"
---
# <a name="resizemode-cell-shape-transform-section"></a>ResizeMode, cellule (section Shape Transform)

Indique le mode de redimensionnement actuel pour la forme.
  
|**Valeur**|**Description**|**Constante d’Automation**|
|:-----|:-----|:-----|
|0  <br/> |Utiliser les paramètres du groupe  <br/> |**visXFormResizeDontCare** <br/> |
|1  <br/> |Repositionner seulement  <br/> |**visXFormResizeSpread** <br/> |
|2  <br/> |Mettre à l'échelle avec le groupe  <br/> |**visXFormResizeScale** <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir cette valeur sur l’onglet **comportement** dans la boîte de dialogue **comportement** (sous l’onglet [développeur](run-in-developer-mode-display-the-developer-tab.md), dans le groupe **Création de la forme** , cliquez sur **comportement**). Pour obtenir une référence à la cellule ResizeMode par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |ResizeMode  <br/> |
   
Pour obtenir une référence à la cellule ResizeMode par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowXFormOut** <br/> |
|Index de la cellule :  <br/> |**visXFormResizeMode** <br/> |
   

