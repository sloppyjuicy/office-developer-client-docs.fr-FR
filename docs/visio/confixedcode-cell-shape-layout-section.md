---
title: ConFixedCode, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm175
ms.localizationpriority: medium
ms.assetid: 8e7c9080-7ef1-0696-a3d2-d8f57ea5ab9b
description: Détermine le repositionnement d'un connecteur.
ms.openlocfilehash: b7d72fd0de48f70290f7ed59d3861cdd06be9213
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560017"
---
# <a name="confixedcode-cell-shape-layout-section"></a>ConFixedCode, cellule (section Shape Layout)

Détermine le repositionnement d'un connecteur.
  
|**Valeur**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
|0  <br/> |Repositionner librement  <br/> |**visSLOConFixedRerouteFreely** <br/> |
|1  <br/> |Repositionner selon les besoins (repositionnement manuel)  <br/> |**visSLOConFixedRerouteAsNeeded** <br/> |
|2  <br/> |Ne jamais repositionner  <br/> |**visSLOConFixedRerouteNever** <br/> |
|3  <br/> |Repositionner en cas de croisement  <br/> |**visSLOConFixedRerouteOnCrossover** <br/> |
|4   <br/> |Réservé à un usage interne  <br/> |**visSLOConFixedByAlgFrom** <br/> |
|5  <br/> |Réservé à un usage interne  <br/> |**visSLOConFixedByAlgTo** <br/> |
|6   <br/> |Réservé à un usage interne  <br/> |**visSLOConFixedByAlgFromTo** <br/> |
   
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
   

