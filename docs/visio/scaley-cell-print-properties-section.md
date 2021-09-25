---
title: ScaleY, cellule (section Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033788
ms.localizationpriority: medium
ms.assetid: 02835aff-455b-ffeb-d53b-28387b6ce361
description: Spécifie le pourcentage d’agrandissement de la page de dessin sur la page d’impression.
ms.openlocfilehash: d4a84ef5a7d9d158ec64bab61cc18ffa6c794b97
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573424"
---
# <a name="scaley-cell-print-properties-section"></a>ScaleY, cellule (section Print Properties)

Spécifie le pourcentage d’agrandissement de la page de dessin sur la page d’impression.
  
## <a name="remarks"></a>Remarques

Cette valeur n’est utilisée que lorsque la valeur de la cellule OnPage est FALSE. Les cellules ScaleX et ScaleY ont toujours la même valeur, ce qui  correspond à la valeur du paramètre  Ajuster à sous l’onglet Configuration de l’impression de la boîte de dialogue Mise en **page** (sous l’onglet Création, cliquez sur la flèche Mise en **page).**  
  
Pour obtenir une référence à la cellule ScaleY par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |ScaleY  <br/> |
   
Pour obtenir une référence à la cellule ScaleY à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowPrintProperties** <br/> |
|Index de la cellule :  <br/> |**visPrintPropertiesScaleY** <br/> |
   

