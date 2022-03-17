---
title: QuickStyleType Cell (Quick Style Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: e7470417-0d70-433e-9496-604ca2eafee6
description: Détermine le type de style rapide (2 dimensions, 1 dimension ou connecteur) dont hérite la forme.
ms.openlocfilehash: 52f547bc70927f37ae6ecfe7c0b9c40d0e633e1a
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63520461"
---
# <a name="quickstyletype-cell-quick-style-section"></a>QuickStyleType Cell (Quick Style Section)

Détermine le type de style rapide (2 dimensions, 1 dimension ou connecteur) dont hérite la forme. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|0  <br/> |Visio choisit automatiquement  <br/> |
|1  <br/> |1 dimension  <br/> |
|2  <br/> |2 dimensions  <br/> |
|3  <br/> |Connector  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **QuickStyleType** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | QuickStyleType  <br/> |
   
Pour obtenir une référence à la **cellule QuickStyleType** à l’aide d’un index à partir d’un programme, utilisez la **propriété CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowQuickStyleProperties** <br/> |
| **Index de la cellule :**  <br/> |**visQuickStyleType** <br/> |
   

