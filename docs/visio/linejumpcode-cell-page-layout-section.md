---
title: LineJumpCode, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm540
localization_priority: Normal
ms.assetid: 56f9043d-a632-65df-c710-45867cce1627
description: Détermine les connecteurs auxquels appliquer des déviations
ms.openlocfilehash: abb7208c2cfbd6b1423e091efc1d526f8b10b57d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788944"
---
# <a name="linejumpcode-cell-page-layout-section"></a>LineJumpCode, cellule (section Page Layout)

Détermine les connecteurs auxquels appliquer des déviations
  
|**Valeur**|**Connecteurs auxquels vous souhaitez ajouter des déviations**|**Constante d’Automation**|
|:-----|:-----|:-----|
|0  <br/> |Aucune  <br/> |**visPLOJumpNone** <br/> |
|1  <br/> |Lignes horizontales  <br/> |**visPLOJumpHorizontal** <br/> |
|2  <br/> |Traits verticaux  <br/> |**visPLOJumpVertical** <br/> |
|3  <br/> |Dernier trait repositionné  <br/> |**visPLOJumpLastRouted** <br/> |
|4  <br/> |Dernier trait affiché (top forme *z* -ordre)  <br/> |**visPLOJumpDisplayOrder** <br/> |
|5  <br/> |Premier trait affiché (forme en bas de *z* -ordre)  <br/> |**visPLOJumpReverseDisplayOrder** <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de cette cellule sous l’onglet **disposition et positionnement** dans la boîte de dialogue **Mise en Page** (sous l’onglet **Création** , cliquez sur la flèche **Mise en Page** , puis cliquez sur **disposition et positionnement**).
  
Pour obtenir une référence à la cellule LineJumpCode par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |LineJumpCode  <br/> |
   
Pour obtenir une référence à la cellule LineJumpCode par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowPageLayout** <br/> |
|Index de la cellule :  <br/> |**visPLOJumpCode** <br/> |
   

