---
title: Bullet, cellule (section Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm130
localization_priority: Normal
ms.assetid: 124a5ee1-6dd1-d17d-6f0e-dbaa5d95d9cd
description: Détermine le style de puce.
ms.openlocfilehash: d3ecdd8e0f3780490f92766351b5ac94e875ae28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788187"
---
# <a name="bullet-cell-paragraph-section"></a>Bullet, cellule (section Paragraph)

Détermine le style de puce.
  
|**Valeur**|**Style de puce**|
|:-----|:-----|
|0  <br/> |Aucune  <br/> |
|1  <br/> |![](media/IC_Bullet1_ZA07645847.gif)           <br/> |
|2  <br/> |![](media/IC_Bullet2_ZA07645848.gif)           <br/> |
|3  <br/> |![](media/IC_Bullet3_ZA07645849.gif)           <br/> |
|4  <br/> |![](media/IC_Bullet4_ZA07645851.gif)           <br/> |
|5  <br/> |![](media/IC_Bullet5_ZA07645852.gif)           <br/> |
|6  <br/> |![](media/IC_Bullet6_ZA07645853.gif)           <br/> |
|7  <br/> |![](media/IC_Bullet7_ZA07645854.gif)           <br/> |
   
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionParagraph** <br/> |
|Index de la ligne :  <br/> |**visRowParagraph** +  *i* où *i* = 0, 1, 2,...  <br/> |
|Index de la cellule :  <br/> |**visBulletIndex** <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de cette cellule en cliquant sur une forme, en pointant sur **Format**, en cliquant sur **texte**, puis en cliquant sur l’onglet **puces** . 
  
Pour obtenir une référence à la cellule Bullet par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |Para.Bullet [ *i* ] où *i* = < 1 >, 2, 3,...  <br/> |
   
Pour obtenir une référence à la cellule Bullet par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  

