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
ms.openlocfilehash: 830a3104361ca985fba888fec781892330d2ff6d
ms.sourcegitcommit: 4164855836af53a068bbbc5b5d126f83ee83e324
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2022
ms.locfileid: "63426775"
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
  
||Valeur |
|:-----|:-----|
|**Nom de la cellule :**  <br/> |LineAdjustTo  <br/> |
   
Pour obtenir une référence à la cellule LineAdjustTo à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRowPageLayout** <br/> |
|**Index de la cellule :**  <br/> |**visPLOLineAdjustTo** <br/> |
   

