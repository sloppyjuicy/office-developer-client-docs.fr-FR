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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404182"
---
# <a name="confixedcode-cell-shape-layout-section"></a>ConFixedCode, cellule (section Shape Layout)

Détermine le repositionnement d'un connecteur.
  
|**Valeur**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
|0  <br/> |Repositionner librement  <br/> |**visSLOConFixedRerouteFreely** <br/> |
|1   <br/> |Repositionner selon les besoins (repositionnement manuel)  <br/> |**visSLOConFixedRerouteAsNeeded** <br/> |
|2   <br/> |Ne jamais repositionner  <br/> |**visSLOConFixedRerouteNever** <br/> |
|3   <br/> |Repositionner en cas de croisement  <br/> |**visSLOConFixedRerouteOnCrossover** <br/> |
|4   <br/> |Réservé à un usage interne  <br/> |**visSLOConFixedByAlgFrom** <br/> |
|5   <br/> |Réservé à un usage interne  <br/> |**visSLOConFixedByAlgTo** <br/> |
|6   <br/> |Réservé à un usage interne  <br/> |**visSLOConFixedByAlgFromTo** <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de cette cellule  en sélectionnant un connecteur [](run-in-developer-mode-display-the-developer-tab.md) dynamique, en cliquant sur Comportement dans le groupe Création de forme sous l’onglet Développeur, puis sur l’onglet **Connecteur.**  
  
Pour obtenir une référence à la cellule ConFixedCode par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |ConFixedCode  <br/> |
   
Pour obtenir une référence à la cellule ConFixedCode à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowShapeLayout** <br/> |
|Index de la cellule :  <br/> |**visSLOConFixedCode** <br/> |
   

