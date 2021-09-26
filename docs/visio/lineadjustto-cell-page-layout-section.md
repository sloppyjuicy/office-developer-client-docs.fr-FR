---
title: LineAdjustTo, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm525
ms.localizationpriority: medium
ms.assetid: 81cd9670-8a6f-824b-528c-e9b88c86f525
description: Indique les connecteurs dynamiques qui se superposent.
ms.openlocfilehash: 5f0d12107f760d9e442ab733fa8a03bb4bda6f55
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618657"
---
# <a name="lineadjustto-cell-page-layout-section"></a>LineAdjustTo, cellule (section Page Layout)

Indique les connecteurs dynamiques qui se superposent.
  
|**Valeur**|**Ajustement**|**Constante d'automation**|
|:-----|:-----|:-----|
|0  <br/> |Style de positionnement par défaut  <br/> |**visPLOLineAdjustToDefault** <br/> |
|1  <br/> |Traits proches les uns des autres  <br/> |**visPLOLineAdjustToAll** <br/> |
|2  <br/> |Aucun trait  <br/> |**visPLOLineAdjustToNone** <br/> |
|3  <br/> |Traits connexes  <br/> |**visPLOLineAdjustToRelated** <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de cette cellule dans l’onglet **Disposition et positionnement** dans la boîte de dialogue **Mise en page** (sous l’onglet **Création**, cliquez sur la flèche **Mise en page**, puis cliquez sur **Disposition et positionnement**).
  
Pour obtenir une référence à la cellule LineAdjustTo par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |LineAdjustTo  <br/> |
   
Pour obtenir une référence à la cellule LineAdjustTo à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowPageLayout** <br/> |
|Index de la cellule :  <br/> |**visPLOLineAdjustTo** <br/> |
   

