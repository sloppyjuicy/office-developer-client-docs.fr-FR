---
title: QuickStyleVariation Cell (Quick Style Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e3b58a19-9f1a-4f2b-9fe2-45cbb7ec6898
description: Détermine s'il faut remplacer les formules et les valeurs de texte, de trait et de couleur de remplissage (ou une combinaison de ces propriétés) à l'aide de couleurs qui contrastent avec l'arrière-plan du diagramme. La valeur est un opérateur de bits or de 0, 1, 2, 4 et 8.
ms.openlocfilehash: 736e2287c00c24774ef8b677613235d642697f4b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433793"
---
# <a name="quickstylevariation-cell-quick-style-section"></a>QuickStyleVariation Cell (Quick Style Section)

Détermine s'il faut remplacer les formules et les valeurs de texte, de trait et de couleur de remplissage (ou une combinaison de ces propriétés) à l'aide de couleurs qui contrastent avec l'arrière-plan du diagramme. La valeur est un opérateur de bits or de 0, 1, 2, 4 et 8.
  
|**Valeur**|**Description**|
|:-----|:-----|
|0  <br/> |Ne modifiez pas le texte, la ligne ou la couleur de remplissage d'une forme (ou n'importe quelle combinaison de ces propriétés) pour qu'elle reste visible par rapport à la couleur d'arrière-plan d'un thème.  <br/> |
|0,1  <br/> |Ne modifiez pas le texte, la ligne ou la couleur de remplissage d'une forme (ou n'importe quelle combinaison de ces propriétés) pour qu'elle reste visible par rapport à la couleur d'arrière-plan d'un thème.  <br/> |
|n°2  <br/> |Modifier la couleur du texte d'une forme, si nécessaire, pour rester visible par rapport à la couleur d'arrière-plan d'un thème donnée.  <br/> |
|4  <br/> |Modifier la couleur de trait d'une forme, si nécessaire, pour rester visible par rapport à la couleur d'arrière-plan d'un thème donnée.  <br/> |
|8bits  <br/> |Modifier la couleur de remplissage d'une forme, si nécessaire, pour rester visible par rapport à la couleur d'arrière-plan d'un thème donnée.  <br/> |
   
## <a name="remarks"></a>Remarques

Utilisez la cellule QuickStyleVariation pour garantir une visibilité en texte ou en lignes lorsqu'elles se trouvent en dehors de toute géométrie de forme visible (par exemple, dans une forme dont la zone de texte se trouve en dessous du bas de la forme, comme celles des diagrammes de réseaux). La valeur par défaut de la cellule est 0, ce qui signifie que son comportement est inactif. Toute autre valeur déclenche le comportement de la cellule.
  
La valeur QuickStyleVariation remplace la valeur produite par la fonction THEMEVAL lorsqu'elle réside dans les cellules Color (section Character), FillForegnd ou LineColor (ou produites par des références directes à ces trois propriétés par le biais de THEMEVAL (" CharacterColor "), THEMEVAL (" FillColor ") et THEMEVAL (" LineColor ")).
  
Pour obtenir une référence à la cellule **QuickStyleVariation** par un nom à partir d'une autre formule, en obtenant la valeur de l'attribut **N** d'un élément de **cellule** ou d'un programme en faisant appel à la propriété **CellsU** , utilisez: 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |QuickStyleVariation  <br/> |
   
Pour obtenir une référence à la cellule **QuickStyleVariation** à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants: 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**Définis** <br/> |
|Index de la ligne :  <br/> |**visRowQuickStyleProperties** <br/> |
|Index de la cellule :  <br/> |**visQuickStyleVariation** <br/> |
   

