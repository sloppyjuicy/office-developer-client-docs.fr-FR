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
ms.openlocfilehash: ebe7dd7ea9cffe1edd48fbad9b027f8f43aaa343
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63523002"
---
# <a name="linejumpstyle-cell-page-layout-section"></a>LineJumpStyle, cellule (section Page Layout)

Détermine le style de déviation de tous les connecteurs de la page de dessin n'ayant pas de style de déviation local.
  
|**Valeur**|**Style de déviation de trait**|**Constante d'automation**|
|:-----|:-----|:-----|
|0  <br/> |Arc  <br/> |**visLOJumpStyleDefault** <br/> |
|1  <br/> |Arc  <br/> |**visLOJumpStyleArc** <br/> |
|2  <br/> |Gap  <br/> |**visLOJumpStyleGap** <br/> |
|3  <br/> |Square  <br/> |**visLOJumpStyleSquare** <br/> |
|4  <br/> |2 côtés  <br/> |**visLOJumpStyleTriangle** <br/> |
|5  <br/> |3 côtés  <br/> |**visLOJumpStyle2Point** <br/> |
|6   <br/> |4 côtés  <br/> |**visLOJumpStyle3Point** <br/> |
|7   <br/> |5 côtés  <br/> |**visLOJumpStyle4Point** <br/> |
|8   <br/> |6 côtés  <br/> |**visLOJumpStyle5Point** <br/> |
|9   <br/> |7 côtés  <br/> |**visLOJumpStyle6Point** <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de cette cellule dans l’onglet **Disposition et positionnement** dans la boîte de dialogue **Mise en page** (sous l’onglet **Création**, cliquez sur la flèche **Mise en page**, puis cliquez sur **Disposition et positionnement**).
  
Pour obtenir une référence à la cellule LineJumpStyle par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de la cellule :**  <br/> |LineJumpStyle  <br/> |
   
Pour obtenir une référence à la cellule LineJumpStyle à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRowPageLayout** <br/> |
|**Index de la cellule :**  <br/> |**visPLOJumpStyle** <br/> |
   

