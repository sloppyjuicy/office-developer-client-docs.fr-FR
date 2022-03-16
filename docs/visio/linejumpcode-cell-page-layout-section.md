---
title: LineJumpCode, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm540
ms.localizationpriority: medium
ms.assetid: 56f9043d-a632-65df-c710-45867cce1627
description: Détermine les connecteurs auxquels appliquer des déviations
ms.openlocfilehash: 0ac7b84be0254eab06c27c64c1381268727190da
ms.sourcegitcommit: b2c5a02b2d0abd2da2542089fc3f83ff07e121e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2022
ms.locfileid: "63506746"
---
# <a name="linejumpcode-cell-page-layout-section"></a>LineJumpCode, cellule (section Page Layout)

Détermine les connecteurs auxquels appliquer des déviations
  
|**Valeur**|**Connecteurs auxquels appliquer des déviations**|**Constante d'automation**|
|:-----|:-----|:-----|
|0  <br/> |Aucun  <br/> |**visPLOJumpNone** <br/> |
|1  <br/> |Lignes horizontales  <br/> |**visPLOJumpHorizontal** <br/> |
|2  <br/> |Traits verticaux  <br/> |**visPLOJumpVertical** <br/> |
|3  <br/> |Dernier trait repositionné  <br/> |**visPLOJumpLastRouted** <br/> |
|4  <br/> |Dernière ligne affichée (forme supérieure dans  *l’ordre de z*  )  <br/> |**visPLOJumpDisplayOrder** <br/> |
|5  <br/> |Première ligne affichée (forme au bas de  *l’ordre de z*  )  <br/> |**visPLOJumpReverseDisplayOrder** <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de cette cellule dans l’onglet **Disposition et positionnement** dans la boîte de dialogue **Mise en page** (sous l’onglet **Création**, cliquez sur la flèche **Mise en page**, puis cliquez sur **Disposition et positionnement**).
  
Pour obtenir une référence à la cellule LineJumpCode par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de la cellule :**  <br/> |LineJumpCode  <br/> |
   
Pour obtenir une référence à la cellule LineJumpCode à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRowPageLayout** <br/> |
|**Index de la cellule :**  <br/> |**visPLOJumpCode** <br/> |
   

