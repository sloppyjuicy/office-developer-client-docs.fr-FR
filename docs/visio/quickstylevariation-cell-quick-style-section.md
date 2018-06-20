---
title: QuickStyleVariation, cellule (Section Style rapide)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e3b58a19-9f1a-4f2b-9fe2-45cbb7ec6898
description: Détermine s’il faut remplacer les formules et les valeurs de texte, ligne et remplissage couleur (ou une combinaison de ces propriétés) à l’aide de couleurs qui contraste avec l’arrière-plan du diagramme. Valeur est une opération de bits OR de 0, 1, 2, 4 et 8.
ms.openlocfilehash: fe6462798b61a0713f98196974876144cf4606e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789386"
---
# <a name="quickstylevariation-cell-quick-style-section"></a>QuickStyleVariation, cellule (Section Style rapide)

Détermine s’il faut remplacer les formules et les valeurs de texte, ligne et remplissage couleur (ou une combinaison de ces propriétés) à l’aide de couleurs qui contraste avec l’arrière-plan du diagramme. Valeur est une opération de bits OR de 0, 1, 2, 4 et 8.
  
|**Valeur**|**Description**|
|:-----|:-----|
|0  <br/> |Ne modifiez pas le texte d’une forme, ligne, ou remplissage couleur (ou n’importe quelle combinaison de ces propriétés) pour restent visibles par rapport à la couleur d’arrière-plan donnée d’un thème.  <br/> |
|1  <br/> |Ne modifiez pas le texte d’une forme, ligne, ou remplissage couleur (ou n’importe quelle combinaison de ces propriétés) pour restent visibles par rapport à la couleur d’arrière-plan donnée d’un thème.  <br/> |
|2  <br/> |Modifier la couleur du texte d’une forme, le cas échéant, reste visible par rapport à d’un thème couleur d’arrière-plan en fonction de le.  <br/> |
|4  <br/> |Modifier la couleur de trait d’une forme, si nécessaire, pour restent visibles auprès d’un thème donné la couleur d’arrière-plan.  <br/> |
|8  <br/> |Modifier la couleur de remplissage d’une forme, si nécessaire, pour restent visibles auprès d’un thème donné la couleur d’arrière-plan.  <br/> |
   
## <a name="remarks"></a>Remarques

Utilisez la cellule QuickStyleVariation afin de garantir la visibilité de texte ou de lignes lorsqu’elles se trouvent en dehors de toute la géométrie des formes visible (par exemple, dans une forme dont textbox est inférieure à la partie inférieure de la forme, telles que celles dans les diagrammes de réseau). La valeur de cellule par défaut est 0, ce qui signifie que son comportement est inactif. Toute autre valeur déclenche le comportement de la cellule.
  
La valeur QuickStyleVariation remplace la valeur générée par la fonction THEMEVAL lorsqu’il réside dans la couleur (Section caractère), FillForegnd ou LineColor cellules (ou générées par des références directes à ces trois propriétés prenait THEMEVAL ( » CharacterColor »), THEMEVAL("FillColor") et THEMEVAL("LineColor")).
  
Pour obtenir une référence à la cellule **QuickStyleVariation** par un nom à partir d’une autre formule, en obtenant la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |QuickStyleVariation  <br/> |
   
Pour obtenir une référence à la cellule **QuickStyleVariation** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowQuickStyleProperties** <br/> |
|Index de la cellule :  <br/> |**visQuickStyleVariation** <br/> |
   

