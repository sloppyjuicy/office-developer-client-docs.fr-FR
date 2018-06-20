---
title: PlaceStyle, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7dcd5a35-bd3d-447f-e4aa-986091d129de
description: Détermine comment les formes sont placées sur la page lorsque vous disposez des formes à l’aide de la boîte de dialogue Configurer la disposition (sous l’onglet Création, dans le groupe mise en page, cliquez sur Re-mise en Page, puis cliquez sur autres Options de mise en page).
ms.openlocfilehash: 251bee427c732fe782c85c4991df07a1deb2a4dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789245"
---
# <a name="placestyle-cell-page-layout-section"></a>PlaceStyle, cellule (section Page Layout)

Détermine comment les formes sont placées sur la page lorsque vous disposez des formes à l’aide de la boîte de dialogue **Configurer la disposition** (sous l’onglet **Création** , dans le groupe **mise en page** , cliquez sur **Re-mise en Page**, puis cliquez sur **Autres Options de mise en page**).
  
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de cette cellule dans la boîte de dialogue **Configurer la disposition** . 
  
Pour obtenir une référence à la cellule PlaceStyle par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |PlaceStyle  <br/> |
   
Pour obtenir une référence à la cellule PlaceStyle par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowPageLayout** <br/> |
|Index de la cellule :  <br/> |**visPLOPlaceStyle** <br/> |
   

