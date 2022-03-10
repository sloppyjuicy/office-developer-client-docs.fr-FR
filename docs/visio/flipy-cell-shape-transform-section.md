---
title: FlipY, cellule (section Shape Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251198
ms.localizationpriority: medium
ms.assetid: 062022ff-e243-2540-becd-d9b969ce83ce
description: Indique si la forme a été retournée verticalement.
ms.openlocfilehash: 4f98e018f871497d6fa14a4be7d8a4df1a36c571
ms.sourcegitcommit: 4164855836af53a068bbbc5b5d126f83ee83e324
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2022
ms.locfileid: "63427181"
---
# <a name="flipy-cell-shape-transform-section"></a>FlipY, cellule (section Shape Transform)

Indique si la forme a été retournée verticalement.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | La forme a été retournée verticalement. |
| FALSE  <br/> | La forme n'a pas été retournée verticalement. |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule FlipY par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de la cellule :**  <br/> | FlipY  <br/> |
   
Pour obtenir une référence à la cellule FlipY à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowXFormOut** <br/> |
| **Index de la cellule :**  <br/> |**visXFormFlipY** <br/> |
   

