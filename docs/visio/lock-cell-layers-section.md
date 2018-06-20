---
title: Lock, cellule (section Layers)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm590
localization_priority: Normal
ms.assetid: 47bb268f-acdd-7369-716c-bd51a32b8a49
description: Indique si les formes appartenant au calque sont verrouillées en sélection ou en modification.
ms.openlocfilehash: f404fe15814de802f4f6bfcebfd2558cf10cc7eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788981"
---
# <a name="lock-cell-layers-section"></a>Lock, cellule (section Layers)

Indique si les formes appartenant au calque sont verrouillées en sélection ou en modification.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Les formes sont verrouillées.  <br/> |
|FALSE  <br/> |Aucune forme n'est verrouillée.  <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir cette valeur en sélectionnant le **verrou** dans la boîte de dialogue **Propriétés des calques** (sous l’onglet **accueil** , dans le groupe **modification** , cliquez sur **calques**, puis cliquez sur **Propriétés des calques**).
  
Pour obtenir une référence à la cellule Lock par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |Layers.Locked [ *i* ] où *i* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule Lock par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionLayer** <br/> |
|Index de la ligne :  <br/> |**visRowLayer** +  *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visLayerLock** <br/> |
   

