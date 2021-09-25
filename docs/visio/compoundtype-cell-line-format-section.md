---
title: CompoundType Cell (Line Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 3e2a88ad-d92c-4550-8da3-fa7fdd032e73
description: Détermine le type composé de la ligne d’une forme.
ms.openlocfilehash: c43175bc42e74bc18b8bf643976fdc859e3dbf8b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608458"
---
# <a name="compoundtype-cell-line-format-section"></a>CompoundType Cell (Line Format Section)

Détermine le type composé de la ligne d’une forme. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|0  <br/> |Simple  <br/> |
|1  <br/> |Double  <br/> |
|2  <br/> |Épaisseur fine  <br/> |
|3  <br/> |Épaisseur fine  <br/> |
|4   <br/> |Triple  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **CompoundType** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU,** utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | CompoundType  <br/> |
   
Pour obtenir une référence à la **cellule CompoundType** à l’aide d’un index à partir d’un programme, utilisez la **propriété CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowLine** <br/> |
| Index de la cellule :  <br/> |**visCompoundType** <br/> |
   

