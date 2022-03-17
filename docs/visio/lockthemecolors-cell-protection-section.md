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
ms.openlocfilehash: e044f37084cc3f69b8db9a760cfa3e0f43d8ae41
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63522386"
---
# <a name="lockthemecolors-cell-protection-section"></a>LockThemeColors, cellule (section Protection)

Empêche l’application de couleurs de thème à la forme. 
  
La valeur de la cellule LockThemeColors correspond au paramétrage de la case à cocher **Contre les couleurs du thème** de la boîte de dialogue **Protection**. 
  
Pour faire référence à la cellule LockThemeColors par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :

 
  
||Valeur |
|:-----|:-----|
|**Nom de la cellule :**  <br/> |LockThemeColors  <br/> |
   
Pour faire référence à la cellule LockThemeColors par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :

 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRowLock** <br/> |
|**Index de la cellule :**  <br/> |**visLockThemeColors** <br/> |
   

