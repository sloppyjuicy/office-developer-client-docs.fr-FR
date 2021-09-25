---
title: ShapePlowCode, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm900
ms.localizationpriority: medium
ms.assetid: acf07fd7-6aa6-1a92-9b7a-bd6fea8a7cb2
description: Détermine si cette forme positionnable se déplace lorsque vous placez une autre forme positionnable à côté d'elle sur la page de dessin.
ms.openlocfilehash: 53b13a7194bf723410e739b83378fd49e13022c6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622913"
---
# <a name="shapeplowcode-cell-shape-layout-section"></a>ShapePlowCode, cellule (section Shape Layout)

Détermine si cette forme positionnable se déplace lorsque vous placez une autre forme positionnable à côté d'elle sur la page de dessin.
  
|**Valeur**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
|0  <br/> |Tracer selon les paramètres de la page.  <br/> |**visSLOPlowDefault** <br/> |
|1  <br/> |Ne tracer aucune forme.  <br/> |**visSLOPlowNever** <br/> |
|2  <br/> |Tracer chaque forme.  <br/> |**visSLOPlowAlways** <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de cette cellule pour  une forme particulière sous l’onglet [](run-in-developer-mode-display-the-developer-tab.md) **Placement** de  la boîte de dialogue Comportement (avec une forme sélectionnée, sous l’onglet Développeur, dans le groupe Création de forme, cliquez sur **Comportement,** puis cliquez sur l’onglet **Placement).** 
  
Pour définir ce comportement pour  *toutes les formes*  de la page de dessin, utilisez la cellule PlowCode de la section Mise en page. 
  
Pour obtenir une référence à la cellule ShapePlowCode par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |ShapePlowCode  <br/> |
   
Pour obtenir une référence à la cellule ShapePlowCode à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowShapeLayout** <br/> |
|Index de la cellule :  <br/> |**visSLOPlowCode** <br/> |
   

