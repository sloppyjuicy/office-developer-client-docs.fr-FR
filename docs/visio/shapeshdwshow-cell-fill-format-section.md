---
title: ShapeShdwShow Cell (Fill Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: ece6c889-9291-40ea-b55a-072acdcb8a52
description: Détermine si la forme affiche une ombre, sous la forme d’un nombre integer de 0 à 2.
ms.openlocfilehash: 29e7d2a7c900518d933899cedc35a00dcc046e65
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598121"
---
# <a name="shapeshdwshow-cell-fill-format-section"></a>ShapeShdwShow Cell (Fill Format Section)

Détermine si la forme affiche une ombre, sous la forme d’un nombre integer de 0 à 2.
  
|**Valeur**|**Description**|
|:-----|:-----|
|0  <br/> |Toujours afficher l’ombre si une ombre est spécifiée. Les ombres des sous-formes ne sont pas affichées.  <br/> |
|1  <br/> |Ne restituer une ombre que si la forme n’a pas de parent. Utilisez des ombres de sous-forme si elles sont regroupées.  <br/> |
|2  <br/> |Toujours afficher une ombre si une ombre est spécifiée. Les ombres des sous-formes sont affichées.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **ShapeShdwShow** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU,** utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | ShapeShdwShow  <br/> |
   
Pour obtenir une référence à la **cellule ShapeShdwShow** à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowFill** <br/> |
| Index de la cellule :  <br/> |**visFillShdwShow** <br/> |
   

