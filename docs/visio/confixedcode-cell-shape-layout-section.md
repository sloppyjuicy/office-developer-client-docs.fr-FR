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
ms.openlocfilehash: b2b9cde309c720493f0e46962b2fe6c2e79545d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284461"
---
# <a name="confixedcode-cell-shape-layout-section"></a>ConFixedCode, cellule (section Shape Layout)

Détermine le repositionnement d'un connecteur.
  
|**Value**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
|0  <br/> |Repositionner librement  <br/> |**visSLOConFixedRerouteFreely** <br/> |
|0,1  <br/> |Repositionner selon les besoins (repositionnement manuel)  <br/> |**visSLOConFixedRerouteAsNeeded** <br/> |
|n°2  <br/> |Ne jamais repositionner  <br/> |**visSLOConFixedRerouteNever** <br/> |
|3  <br/> |Repositionner en cas de croisement  <br/> |**visSLOConFixedRerouteOnCrossover** <br/> |
|4  <br/> |Réservé à un usage interne  <br/> |**visSLOConFixedByAlgFrom** <br/> |
|disque  <br/> |Réservé à un usage interne  <br/> |**visSLOConFixedByAlgTo** <br/> |
|6.x  <br/> |Réservé à un usage interne  <br/> |**visSLOConFixedByAlgFromTo** <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de cette cellule en sélectionnant un connecteur dynamique, en cliquant sur **comportement** dans le groupe **création de forme** de l'onglet [développeur](run-in-developer-mode-display-the-developer-tab.md) , puis en cliquant sur l'onglet **connecteur** . 
  
Pour obtenir une référence à la cellule ConFixedCode par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |ConFixedCode  <br/> |
   
Pour obtenir une référence à la cellule ConFixedCode à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**Définis** <br/> |
|Index de la ligne :  <br/> |**visRowShapeLayout** <br/> |
|Index de la cellule :  <br/> |**visSLOConFixedCode** <br/> |
   

