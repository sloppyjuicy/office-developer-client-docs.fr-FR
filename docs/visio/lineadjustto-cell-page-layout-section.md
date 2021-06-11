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
ms.openlocfilehash: e4fb32c0fcb488173324ea597edc2c9d13f6bfca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414024"
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
   

