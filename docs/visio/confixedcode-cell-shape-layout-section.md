---
title: ConFixedCode, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm175
localization_priority: Normal
ms.assetid: 8e7c9080-7ef1-0696-a3d2-d8f57ea5ab9b
description: Détermine le repositionnement d'un connecteur.
ms.openlocfilehash: 448e721d8dd6e287c61488e28b875f76d0fa2977
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788329"
---
# <a name="confixedcode-cell-shape-layout-section"></a>ConFixedCode, cellule (section Shape Layout)

Détermine le repositionnement d'un connecteur.
  
|**Valeur**|**Description**|**Constante d’Automation**|
|:-----|:-----|:-----|
|0  <br/> |Repositionner librement  <br/> |**visSLOConFixedRerouteFreely** <br/> |
|1  <br/> |Repositionner selon les besoins (repositionnement manuel)  <br/> |**visSLOConFixedRerouteAsNeeded** <br/> |
|2  <br/> |Ne jamais repositionner  <br/> |**visSLOConFixedRerouteNever** <br/> |
|3  <br/> |Repositionner en cas de croisement  <br/> |**visSLOConFixedRerouteOnCrossover** <br/> |
|4  <br/> |À usage interne uniquement  <br/> |**visSLOConFixedByAlgFrom** <br/> |
|5  <br/> |À usage interne uniquement  <br/> |**visSLOConFixedByAlgTo** <br/> |
|6  <br/> |À usage interne uniquement  <br/> |**visSLOConFixedByAlgFromTo** <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de cette cellule en sélectionnant un connecteur dynamique et en cliquant sur **comportement** dans le groupe **Création de la forme** sous l’onglet [développeur](run-in-developer-mode-display-the-developer-tab.md) , puis en cliquant sur l’onglet **connecteur** . 
  
Pour obtenir une référence à la cellule ConFixedCode par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |ConFixedCode  <br/> |
   
Pour obtenir une référence à la cellule ConFixedCode par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowShapeLayout** <br/> |
|Index de la cellule :  <br/> |**visSLOConFixedCode** <br/> |
   

