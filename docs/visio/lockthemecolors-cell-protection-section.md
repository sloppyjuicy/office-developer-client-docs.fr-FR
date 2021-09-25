---
title: LockThemeColors, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm70001
ms.localizationpriority: medium
ms.assetid: 22cedeb3-58b5-3932-9252-5c9dd3e163e3
ms.openlocfilehash: e4a96cab2939c17980a7f0daba6af65ddcac4045
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623375"
---
# <a name="lockthemecolors-cell-protection-section"></a>LockThemeColors, cellule (section Protection)

Empêche l’application de couleurs de thème à la forme. 
  
La valeur de la cellule LockThemeColors correspond au paramétrage de la case à cocher **Contre les couleurs du thème** de la boîte de dialogue **Protection**. 
  
Pour faire référence à la cellule LockThemeColors par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :

 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |LockThemeColors  <br/> |
   
Pour faire référence à la cellule LockThemeColors par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowLock** <br/> |
|Index de la cellule :  <br/> |**visLockThemeColors** <br/> |
   

