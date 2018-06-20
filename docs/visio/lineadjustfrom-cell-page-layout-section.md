---
title: LineAdjustFrom, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251887
localization_priority: Normal
ms.assetid: 6949c717-dc69-1d17-5215-eb6efce56fcb
description: Détermine quels connecteurs dynamiques doivent être espacés par l'application s'ils sont positionnés les uns sur les autres.
ms.openlocfilehash: ee3a107f7e19b53017c2ea24c94babceb49620d1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788936"
---
# <a name="lineadjustfrom-cell-page-layout-section"></a>LineAdjustFrom, cellule (section Page Layout)

Détermine quels connecteurs dynamiques doivent être espacés par l'application s'ils sont positionnés les uns sur les autres.
  
|**Valeur**|**Ajustement**|**Constante d’Automation**|
|:-----|:-----|:-----|
|0  <br/> |Traits sans relation  <br/> |**visPLOLineAdjustFromNotRelated** <br/> |
|1  <br/> |Tous les traits  <br/> |**visPLOLineAdjustFromAll** <br/> |
|2  <br/> |Aucun trait  <br/> |**visPLOLineAdjustFromNone** <br/> |
|3  <br/> |Style de positionnement par défaut  <br/> |**visPLOLineAdjustFromRoutingDefault** <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de cette cellule sous l’onglet **disposition et positionnement** dans la boîte de dialogue **Mise en Page** (sous l’onglet **Création** , cliquez sur la flèche **Mise en Page** , puis cliquez sur **disposition et positionnement**).
  
Pour obtenir une référence à la cellule LineAdjustFrom par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |LineAdjustFrom  <br/> |
   
Pour obtenir une référence à la cellule LineAdjustFrom par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowPageLayout** <br/> |
|Index de la cellule :  <br/> |**visPLOLineAdjustFrom** <br/> |
   

