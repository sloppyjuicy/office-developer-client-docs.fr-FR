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
ms.openlocfilehash: 3a54dabb092f9d09ce537e0de494fb243a0f0e7a
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62774341"
---
# <a name="enablegrid-cell-page-layout-section"></a>EnableGrid, cellule (section Page Layout)

Détermine si l’application aligne les formes sur une grille de page interne invisible lorsque vous configurez la disposition dans la boîte de dialogue **Configurer la disposition**. (Sous l’onglet **Création**, dans le groupe **Disposition**, cliquez sur **Nouvelle disposition de page**, puis cliquez sur **Autres options de disposition**.)
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Utilise la grille de page interne. |
|FALSE  <br/> |N'utilise pas la grille de page interne. |
   
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
   

