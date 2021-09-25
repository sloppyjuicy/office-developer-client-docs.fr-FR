---
title: EnableGrid, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251642
ms.localizationpriority: medium
ms.assetid: bfea4ef4-1b30-eb22-215d-3b9b73098da9
description: Détermine si l’application aligne les formes sur une grille de page interne invisible lorsque vous configurez la disposition dans la boîte de dialogue Configurer la disposition. (Sous l’onglet Création, dans le groupe Disposition, cliquez sur Nouvelle disposition de page, puis cliquez sur Autres options de disposition.)
ms.openlocfilehash: f80678446fdb270149f55b2d537237108c9d54f9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570714"
---
# <a name="enablegrid-cell-page-layout-section"></a>EnableGrid, cellule (section Page Layout)

Détermine si l’application aligne les formes sur une grille de page interne invisible lorsque vous configurez la disposition dans la boîte de dialogue **Configurer la disposition**. (Sous l’onglet **Création**, dans le groupe **Disposition**, cliquez sur **Nouvelle disposition de page**, puis cliquez sur **Autres options de disposition**.)
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Utilise la grille de page interne.  <br/> |
|FALSE  <br/> |N'utilise pas la grille de page interne.  <br/> |
   
## <a name="remarks"></a>Remarques

Vous créez cette grille de page au moyen des valeurs **Espace entre les formes** et **Taille de forme moyenne** dans la boîte de dialogue **Espacement : disposition et positionnement**. (Sous l’onglet **Création**, cliquez sur la flèche **Mise en page**, cliquez sur **Disposition et positionnement**, puis cliquez sur **Espacement**.) 
  
Lorsque vous activez cette fonction, l'application aligne le point central de chaque forme positionnable sur le centre d'un bloc de la grille de page interne. 
  
Pour obtenir une référence à la cellule EnableGrid par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |EnableGrid  <br/> |
   
Pour obtenir une référence à la cellule EnableGrid à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowPageLayout** <br/> |
|Index de la cellule :  <br/> |**visPLOEnableGrid** <br/> |
   

