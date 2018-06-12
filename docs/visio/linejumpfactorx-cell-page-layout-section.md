---
title: LineJumpFactorX, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm545
localization_priority: Normal
ms.assetid: 0649672f-f496-ce80-6dc3-3affc9b6f913
description: Détermine la taille des déviations sur les connecteurs dynamiques horizontaux de la page par rapport à la valeur de la cellule LineToLineX. La valeur de cette cellule est comprise entre 0 et 10 mais des valeurs fractionnelles de 0 à 1 sont proposées.
ms.openlocfilehash: fb6205407070485a0e234ee594e84979bca40891
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788943"
---
# <a name="linejumpfactorx-cell-page-layout-section"></a>LineJumpFactorX, cellule (section Page Layout)

Détermine la taille des déviations sur les connecteurs dynamiques horizontaux de la page par rapport à la valeur de la cellule LineToLineX. La valeur de cette cellule est comprise entre 0 et 10 mais des valeurs fractionnelles de 0 à 1 sont proposées.
  
## <a name="remarks"></a>Note

Vous pouvez également définir la valeur de cette cellule sous l’onglet **disposition et positionnement** dans la boîte de dialogue **Mise en Page** (sous l’onglet **Création** , cliquez sur la flèche **Mise en Page** , puis cliquez sur **disposition et positionnement**).
  
Pour obtenir une référence à la cellule LineJumpFactorX par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |LineJumpFactorX  <br/> |
   
Pour obtenir une référence à la cellule LineJumpFactorX par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowPageLayout** <br/> |
|Index de la cellule :  <br/> |**visPLOJumpFactorX** <br/> |
   

