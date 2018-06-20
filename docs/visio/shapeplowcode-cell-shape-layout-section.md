---
title: ShapePlowCode, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm900
localization_priority: Normal
ms.assetid: acf07fd7-6aa6-1a92-9b7a-bd6fea8a7cb2
description: Détermine si cette forme positionnable se déplace lorsque vous placez une autre forme positionnable à côté d'elle sur la page de dessin.
ms.openlocfilehash: 5917abad653e7aaf40da05eafa3f9f1a90a2cf9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789661"
---
# <a name="shapeplowcode-cell-shape-layout-section"></a>ShapePlowCode, cellule (section Shape Layout)

Détermine si cette forme positionnable se déplace lorsque vous placez une autre forme positionnable à côté d'elle sur la page de dessin.
  
|**Valeur**|**Description**|**Constante d’Automation**|
|:-----|:-----|:-----|
|0  <br/> |Tracer selon les paramètres de la page.  <br/> |**visSLOPlowDefault** <br/> |
|1  <br/> |Ne tracer aucune forme.  <br/> |**visSLOPlowNever** <br/> |
|2  <br/> |Tracer chaque forme.  <br/> |**visSLOPlowAlways** <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de cette cellule pour une forme donnée dans l’onglet **Placement** dans la boîte de dialogue **comportement** (avec la forme sélectionnée, sous l’onglet [développeur](run-in-developer-mode-display-the-developer-tab.md) , dans le groupe **Création de la forme** , cliquez sur **comportement**, puis cliquez sur le Onglet **emplacement** ). 
  
Pour définir ce comportement pour *toutes* les formes sur la page de dessin, utilisez la cellule PlowCode de la section Page Layout. 
  
Pour obtenir une référence à la cellule ShapePlowCode par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |ShapePlowCode  <br/> |
   
Pour obtenir une référence à la cellule ShapePlowCode par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowShapeLayout** <br/> |
|Index de la cellule :  <br/> |**visSLOPlowCode** <br/> |
   

