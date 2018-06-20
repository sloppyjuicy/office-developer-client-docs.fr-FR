---
title: ConLineJumpCode, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251652
localization_priority: Normal
ms.assetid: af85588e-8e83-5168-7a8c-d7e8b4af5c27
description: Détermine la déviation des traits de connecteurs.
ms.openlocfilehash: 002f628841356ec8a22afbb9d4aeca8236058222
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788335"
---
# <a name="conlinejumpcode-cell-shape-layout-section"></a>ConLineJumpCode, cellule (section Shape Layout)

Détermine la déviation des traits de connecteurs.
  
|**Valeur**|**Description**|**Constante d’Automation**|
|:-----|:-----|:-----|
|0  <br/> |Selon la page ; sous l’onglet **Création** , cliquez sur la flèche dans le groupe **Mise en Page** , puis cliquez sur l’onglet **disposition et positionnement** pour afficher les spécifications de la page  <br/> |**visSLOJumpDefault** <br/> |
|1  <br/> |Jamais  <br/> |**visSLOJumpNever** <br/> |
|2  <br/> |Always (Toujours)  <br/> |**visSLOJumpAlways** <br/> |
|3  <br/> |L'autre connecteur est dévié  <br/> |**visSLOJumpOther** <br/> |
|4  <br/> |Aucun connecteur n’est dévié  <br/> |**visSLOJumpNeither** <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de cette cellule en sélectionnant un connecteur dynamique et en cliquant sur **comportement** dans le groupe **Création de la forme** sous l’onglet [développeur](run-in-developer-mode-display-the-developer-tab.md) , puis en cliquant sur l’onglet **connecteur** . 
  
Pour obtenir une référence à la cellule ConLineJumpCode par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |ConLineJumpCode  <br/> |
   
Pour obtenir une référence à la cellule ConLineJumpCode par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowShapeLayout** <br/> |
|Index de la cellule :  <br/> |**visSLOJumpCode** <br/> |
   

