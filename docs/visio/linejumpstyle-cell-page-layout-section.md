---
title: LineJumpStyle, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251646
ms.localizationpriority: medium
ms.assetid: 89f16674-ee1f-f5f9-9830-7bcc52e3a068
description: Détermine le style de déviation de tous les connecteurs de la page de dessin n'ayant pas de style de déviation local.
ms.openlocfilehash: 78f1003c5f1afac945edd31bf82fb64732b8da1e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603668"
---
# <a name="linejumpstyle-cell-page-layout-section"></a>LineJumpStyle, cellule (section Page Layout)

Détermine le style de déviation de tous les connecteurs de la page de dessin n'ayant pas de style de déviation local.
  
|**Valeur**|**Style de déviation de trait**|**Constante d'automation**|
|:-----|:-----|:-----|
|0  <br/> |Arc  <br/> |**visLOJumpStyleDefault** <br/> |
|1  <br/> |Arc  <br/> |**visLOJumpStyleArc** <br/> |
|2  <br/> |Gap  <br/> |**visLOJumpStyleGap** <br/> |
|3  <br/> |Square  <br/> |**visLOJumpStyleSquare** <br/> |
|4   <br/> |2 côtés  <br/> |**visLOJumpStyleTriangle** <br/> |
|5  <br/> |3 côtés  <br/> |**visLOJumpStyle2Point** <br/> |
|6   <br/> |4 côtés  <br/> |**visLOJumpStyle3Point** <br/> |
|7   <br/> |5 côtés  <br/> |**visLOJumpStyle4Point** <br/> |
|8   <br/> |6 côtés  <br/> |**visLOJumpStyle5Point** <br/> |
|9   <br/> |7 côtés  <br/> |**visLOJumpStyle6Point** <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de cette cellule dans l’onglet **Disposition et positionnement** dans la boîte de dialogue **Mise en page** (sous l’onglet **Création**, cliquez sur la flèche **Mise en page**, puis cliquez sur **Disposition et positionnement**).
  
Pour obtenir une référence à la cellule LineJumpStyle par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |LineJumpStyle  <br/> |
   
Pour obtenir une référence à la cellule LineJumpStyle à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowPageLayout** <br/> |
|Index de la cellule :  <br/> |**visPLOJumpStyle** <br/> |
   

