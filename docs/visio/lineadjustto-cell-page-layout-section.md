---
title: LineAdjustTo, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm525
localization_priority: Normal
ms.assetid: 81cd9670-8a6f-824b-528c-e9b88c86f525
description: Indique les connecteurs dynamiques qui se superposent.
ms.openlocfilehash: 13540f9dc5e6e6861d3f3679bcf49204d553397a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788947"
---
# <a name="lineadjustto-cell-page-layout-section"></a>LineAdjustTo, cellule (section Page Layout)

Indique les connecteurs dynamiques qui se superposent.
  
|**Valeur**|**Ajustement**|**Constante d’Automation**|
|:-----|:-----|:-----|
|0  <br/> |Style de positionnement par défaut  <br/> |**visPLOLineAdjustToDefault** <br/> |
|1  <br/> |Traits proches les uns des autres  <br/> |**visPLOLineAdjustToAll** <br/> |
|2  <br/> |Aucun trait  <br/> |**visPLOLineAdjustToNone** <br/> |
|3  <br/> |Traits connexes  <br/> |**visPLOLineAdjustToRelated** <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de cette cellule sous l’onglet **disposition et positionnement** dans la boîte de dialogue **Mise en Page** (sous l’onglet **Création** , cliquez sur la flèche **Mise en Page** , puis cliquez sur **disposition et positionnement**).
  
Pour obtenir une référence à la cellule LineAdjustTo par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |LineAdjustTo  <br/> |
   
Pour obtenir une référence à la cellule LineAdjustTo par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowPageLayout** <br/> |
|Index de la cellule :  <br/> |**visPLOLineAdjustTo** <br/> |
   

