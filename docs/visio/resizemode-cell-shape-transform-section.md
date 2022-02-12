---
title: ResizeMode, cellule (section Shape Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251203
ms.localizationpriority: medium
ms.assetid: 49816e46-fa83-3ee4-1451-9c85fbd0f519
description: Indique le mode de redimensionnement actuel pour la forme.
ms.openlocfilehash: 34aa13ca917bbaecc4494fa2db1acd5eb4e73bf8
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62770393"
---
# <a name="resizemode-cell-shape-transform-section"></a>ResizeMode, cellule (section Shape Transform)

Indique le mode de redimensionnement actuel pour la forme.
  
|**Valeur**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
|0  <br/> |Utiliser les paramètres du groupe |**visXFormResizeDontCare** <br/> |
|1  <br/> |Repositionner seulement |**visXFormResizeSpread** <br/> |
|2  <br/> |Mettre à l'échelle avec le groupe |**visXFormResizeScale** <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir cette valeur sous l’onglet Comportement de  la boîte de dialogue Comportement (dans [l’onglet](run-in-developer-mode-display-the-developer-tab.md) Développeur, dans le groupe Création de formes, cliquez sur **Comportement**). Pour obtenir une référence à la cellule ResizeMode par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |ResizeMode  <br/> |
   
Pour obtenir une référence à la cellule ResizeMode à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowXFormOut** <br/> |
|Index de la cellule :  <br/> |**visXFormResizeMode** <br/> |
   

