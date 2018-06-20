---
title: LineToNodeX, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm575
localization_priority: Normal
ms.assetid: 9d58e23e-b411-c5c1-b785-5014488d42c8
description: Définit l'écart horizontal entre tous les connecteurs et les formes de la page de dessin.
ms.openlocfilehash: 75f7e8150711421138a01175be34003d124e88ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788964"
---
# <a name="linetonodex-cell-page-layout-section"></a>LineToNodeX, cellule (section Page Layout)

Définit l'écart horizontal entre tous les connecteurs et les formes de la page de dessin.
  
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de cette cellule dans la boîte de dialogue **disposition et positionnement** . (Sous l’onglet **Création** , cliquez sur la flèche **Mise en Page** , cliquez sur **disposition et positionnement**, puis cliquez sur **espacement**.)
  
Pour obtenir une référence à la cellule LineToNodeY par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |LineToNodeX  <br/> |
   
Pour obtenir une référence à la cellule LineToNodeX par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowPageLayout** <br/> |
|Index de la cellule :  <br/> |**visPLOLineToNodeX** <br/> |
   

