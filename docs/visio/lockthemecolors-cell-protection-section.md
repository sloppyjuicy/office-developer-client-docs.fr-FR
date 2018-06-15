---
title: LockThemeColors, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm70001
localization_priority: Normal
ms.assetid: 22cedeb3-58b5-3932-9252-5c9dd3e163e3
ms.openlocfilehash: 2ca8af2c7a41259af73a111af331ce1031e5f46c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19789021"
---
# <a name="lockthemecolors-cell-protection-section"></a>LockThemeColors, cellule (section Protection)

Empêche l’application des couleurs de thème à la forme. 
  
La valeur de la cellule LockThemeColors correspond au paramètre **de couleurs de thème** case à cocher dans la boîte de dialogue **Protection** . 
  
Pour faire référence à la cellule LockThemeColors par un nom à partir d’une autre formule ou d’un programme, utilisez la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |LockThemeColors  <br/> |
   
Pour faire référence à la cellule LockThemeColors par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowLock** <br/> |
|Index de la cellule :  <br/> |**visLockThemeColors** <br/> |
   

