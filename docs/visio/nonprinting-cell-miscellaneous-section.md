---
title: NonPrinting, cellule (section Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251321
ms.localizationpriority: medium
ms.assetid: 59fe0887-2092-4fad-ea38-2aba354f3b92
description: Active ou désactive l'impression de la forme sélectionnée.
ms.openlocfilehash: 9812a995ddc027de4c7c7d02a5d74fdbac610092
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62777129"
---
# <a name="nonprinting-cell-miscellaneous-section"></a>NonPrinting, cellule (section Miscellaneous)

Active ou désactive l'impression de la forme sélectionnée.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | L'impression est désactivée mais la forme est affichée dans la fenêtre de dessin. |
| FALSE  <br/> | L'impression est activée. |
   
## <a name="remarks"></a>Remarques

Pour imprimer un repère, sélectionnez-le, puis affectez la valeur FALSE à la cellule NonPrinting.
  
Pour obtenir une référence à la cellule NonPrinting par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | NonPrinting  <br/> |
   
Pour obtenir une référence à la cellule NonPrinting à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section  :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowMisc** <br/> |
| Index de la cellule :  <br/> |**visNonPrinting** <br/> |
   

