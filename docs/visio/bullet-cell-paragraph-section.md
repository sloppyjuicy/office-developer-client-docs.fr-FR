---
title: Bullet, cellule (section Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm130
ms.localizationpriority: medium
ms.assetid: 124a5ee1-6dd1-d17d-6f0e-dbaa5d95d9cd
description: Détermine le style de puce.
ms.openlocfilehash: b20b09cbf9785eb6bd988961f55097bd5fac34d7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554823"
---
# <a name="bullet-cell-paragraph-section"></a>Bullet, cellule (section Paragraph)

Détermine le style de puce.
  
|**Valeur**|**Style de puce**|
|:-----|:-----|
|0  <br/> |Aucun  <br/> |
|1  <br/> |![](media/IC_Bullet1_ZA07645847.gif)           <br/> |
|2  <br/> |![](media/IC_Bullet2_ZA07645848.gif)           <br/> |
|3  <br/> |![](media/IC_Bullet3_ZA07645849.gif)           <br/> |
|4   <br/> |![](media/IC_Bullet4_ZA07645851.gif)           <br/> |
|5  <br/> |![](media/IC_Bullet5_ZA07645852.gif)           <br/> |
|6   <br/> |![](media/IC_Bullet6_ZA07645853.gif)           <br/> |
|7   <br/> |![](media/IC_Bullet7_ZA07645854.gif)           <br/> |
   
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionParagraph** <br/> |
|Index de la ligne :  <br/> |**visRowParagraph**  +   *i* où *i* = 0, 1, 2, ...  <br/> |
|Index de la cellule :  <br/> |**visBulletIndex** <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de cette cellule en cliquant avec le bouton droit sur une forme, en pointant sur **Format**, en cliquant sur **Texte**, puis en cliquant sur l’onglet **Puces**. 
  
Pour obtenir une référence à la cellule Bullet par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |Para.Bullet[ *i*  ] où  *i*  = <1>, 2, 3, ...  <br/> |
   
Pour obtenir une référence à la cellule Bullet par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  

