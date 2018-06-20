---
title: AvenueSizeX, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm65
localization_priority: Normal
ms.assetid: 86fe25ed-590d-b2f0-5dfe-9746a19c6b04
description: Détermine la quantité d’espace horizontal entre les formes sur la page de dessin lorsque vous les disposez à l’aide de la boîte de dialogue Configurer la disposition (sous l’onglet Création, dans le groupe mise en page, cliquez sur Re-mise en Page, puis cliquez sur autres Options de mise en page).
ms.openlocfilehash: efb29181414957063e038b97c2d7b79720aa0405
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788052"
---
# <a name="avenuesizex-cell-page-layout-section"></a>AvenueSizeX, cellule (section Page Layout)

Détermine la quantité d’espace horizontal entre les formes sur la page de dessin lorsque vous les disposez à l’aide de la boîte de dialogue **Configurer la disposition** (sous l’onglet **Création** , dans le groupe **mise en page** , cliquez sur **Re-mise en Page**, puis cliquez sur ** plus Options de disposition **).
  
## <a name="remarks"></a>Remarques

Vous pouvez également définir cette valeur dans la boîte de dialogue **disposition et positionnement** (sous l’onglet **Création** , cliquez sur la flèche dans le groupe **Mise en Page** , cliquez sur l’onglet **disposition et positionnement** , puis cliquez sur **espacement**).
  
La grille dynamique utilise le paramètre dans la cellule AvenueSizeX lorsque qu’une seule forme est disponible pour calculer l’espacement horizontal. Pour utiliser la grille dynamique, sous l’onglet **affichage** , dans le groupe **aides visuelles** , sélectionnez **Grille dynamique**.
  
Pour obtenir une référence à la cellule AvenueSizeX par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | AvenueSizeY  <br/> |
   
Pour obtenir une référence à la cellule AvenueSizeX par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowPageLayout** <br/> |
| Index de la cellule :  <br/> |**visPLOAvenueSizeX** <br/> |
   

