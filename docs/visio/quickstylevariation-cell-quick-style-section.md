---
title: QuickStyleVariation Cell (Quick Style Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: e3b58a19-9f1a-4f2b-9fe2-45cbb7ec6898
description: Détermine s’il faut remplacer les formules et les valeurs de texte, de trait et de couleur de remplissage (ou une combinaison de ces propriétés) à l’aide de couleurs qui contrastent avec l’arrière-plan du diagramme. La valeur est un OR au bit de 0, 1, 2, 4 et 8.
ms.openlocfilehash: 8d4ba0cfb203da3e69bb1a1f4110d44ac2db8cd4
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63523492"
---
# <a name="quickstylevariation-cell-quick-style-section"></a>QuickStyleVariation Cell (Quick Style Section)

Détermine s’il faut remplacer les formules et les valeurs de texte, de trait et de couleur de remplissage (ou une combinaison de ces propriétés) à l’aide de couleurs qui contrastent avec l’arrière-plan du diagramme. La valeur est un OR au bit de 0, 1, 2, 4 et 8.
  
|**Valeur**|**Description**|
|:-----|:-----|
|0  <br/> |Ne modifiez pas la couleur de texte, de trait ou de remplissage d’une forme (ou toute combinaison de ces propriétés) pour rester visible par rapport à la couleur d’arrière-plan donnée d’un thème. |
|1  <br/> |Ne modifiez pas la couleur de texte, de trait ou de remplissage d’une forme (ou toute combinaison de ces propriétés) pour rester visible par rapport à la couleur d’arrière-plan donnée d’un thème. |
|2  <br/> |Modifiez la couleur de texte d’une forme, si nécessaire, pour qu’elle reste visible par rapport à la couleur d’arrière-plan donnée d’un thème. |
|4  <br/> |Modifiez la couleur de trait d’une forme, si nécessaire, pour qu’elle reste visible par rapport à la couleur d’arrière-plan donnée d’un thème. |
|8   <br/> |Modifiez la couleur de remplissage d’une forme, si nécessaire, pour qu’elle reste visible par rapport à la couleur d’arrière-plan donnée d’un thème. |
   
## <a name="remarks"></a>Remarques

Utilisez la cellule QuickStyleVariation pour garantir la visibilité dans le texte ou les lignes lorsqu’elles se trouve en dehors de toute géométrie de forme visible (par exemple, dans une forme dont la boîte de texte se trouve en dessous de la partie inférieure de la forme, comme celles des diagrammes réseau). La valeur par défaut de la cellule est 0, ce qui signifie que son comportement est inactif. Toute autre valeur déclenche le comportement de la cellule.
  
La valeur QuickStyleVariation remplace la valeur produite par la fonction THEMEVAL lorsqu’elle réside dans les cellules Color (Character Section), FillForegnd ou LineColor (ou produite par des références directes à ces trois propriétés au moyen de THEMEVAL(« CharacterColor »), THEMEVAL(« FillColor ») et THEMEVAL(« LineColor »)).
  
Pour obtenir une référence à la cellule **QuickStyleVariation** par un nom à partir d’une autre formule, en obtenant la valeur de l’attribut **N** d’un élément **Cell** ou d’un programme à l’aide de la propriété **CellsU** , utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de cellule :**  <br/> |QuickStyleVariation  <br/> |
   
Pour obtenir une référence à la **cellule QuickStyleVariation** à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRowQuickStyleProperties** <br/> |
|**Index de la cellule :**  <br/> |**visQuickStyleVariation** <br/> |
   

