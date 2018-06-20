---
title: EnableGrid, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251642
localization_priority: Normal
ms.assetid: bfea4ef4-1b30-eb22-215d-3b9b73098da9
description: Détermine si l’application aligne les formes sur une grille de page interne invisible lorsque vous configurez la mise en page dans la boîte de dialogue Configurer la disposition. (Sous l’onglet Création, dans le groupe mise en page, cliquez sur Re-mise en Page, puis cliquez sur autres Options de disposition.)
ms.openlocfilehash: 3371767343132219ebc38134b93afd1da46c7a45
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788551"
---
# <a name="enablegrid-cell-page-layout-section"></a>EnableGrid, cellule (section Page Layout)

Détermine si l’application aligne les formes sur une grille de page interne invisible lorsque vous configurez la mise en page dans la boîte de dialogue **Configurer la disposition** . (Sous l’onglet **Création** , dans le groupe **mise en page** , cliquez sur **Re-mise en Page**, puis cliquez sur **Autres Options de disposition**.)
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Utilise la grille de page interne.  <br/> |
|FALSE  <br/> |N'utilise pas la grille de page interne.  <br/> |
   
## <a name="remarks"></a>Remarques

Vous créez cette grille de page à l’aide de l' **espace entre les formes** et les valeurs de **taille moyenne des formes** dans la boîte de dialogue **disposition et positionnement** . (Sous l’onglet **Création** , cliquez sur la flèche **Mise en Page** , cliquez sur **disposition et positionnement**, puis cliquez sur **espacement**.) 
  
Lorsque vous activez cette fonction, l'application aligne le point central de chaque forme positionnable sur le centre d'un bloc de la grille de page interne. 
  
Pour obtenir une référence à la cellule EnableGrid par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |EnableGrid  <br/> |
   
Pour obtenir une référence à la cellule EnableGrid par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowPageLayout** <br/> |
|Index de la cellule :  <br/> |**visPLOEnableGrid** <br/> |
   

