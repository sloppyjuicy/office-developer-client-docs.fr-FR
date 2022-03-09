---
title: UseGroupGradient Cell (Gradient Properties Section)
manager: lindalu
ms.date: 03/09/2022
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: f1dcf0ec-8b4a-4ee1-9208-b1c84e30d37b
description: Détermine si la forme prend un dégradé lorsque la forme est regroupée avec d’autres formes, sous la forme d’un booléen. La valeur de la cellule UseGroupGradient affecte uniquement le remplissage de la forme.
ms.openlocfilehash: e3ec8556bbdfa20a41d9d1765b0f21a499d4a6d6
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63405608"
---
# <a name="usegroupgradient-cell-gradient-properties-section"></a>UseGroupGradient Cell (Gradient Properties Section)

Détermine si la forme prend un dégradé lorsque la forme est regroupée avec d’autres formes, sous la forme d’un booléen. La valeur de **la cellule UseGroupGradient** affecte uniquement le remplissage de la forme.
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **UseGroupGradient** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU** , utilisez :
  
|**Valeur**|**Description**|
|:-----|:-----|
| Nom de cellule :  <br/> | UseGroupGradient  <br/> |

Pour obtenir une référence à la **cellule UseGroupGradient** à l’aide d’un index à partir d’un programme, utilisez la **propriété CellsSRC** avec les arguments suivants :
  
|**Valeur**|**Description**|
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowGradientProperties** <br/> |
| Index de la cellule :  <br/> |**visUseGroupGradient** <br/> |
