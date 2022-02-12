---
title: Invisible, cellule (section Shape Data)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251341
ms.localizationpriority: medium
ms.assetid: 5f368c2e-2a40-38ee-3568-ed5c57633345
description: Détermine si l’élément de données de forme est visible ou non dans la fenêtre Données de forme.
ms.openlocfilehash: 9d9a5244369cd89187186f319098dc7303b24464
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62775674"
---
# <a name="invisible-cell-shape-data-section"></a>Invisible, cellule (section Shape Data)

Détermine si l’élément de données de forme est visible ou non dans la fenêtre **Données de forme**. 
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | Les données de forme ne sont pas visibles. |
| FALSE  <br/> | L'élément de données de forme est visible. |
   
## <a name="remarks"></a>Remarques

La valeur de cette cellule correspond à la case à cocher **Masquer** dans la boîte de dialogue **Définir les données de forme** (cliquez avec le bouton droit sur la forme, pointez sur **Données**, puis cliquez sur **Définir les données de forme**).
  
Pour obtenir une référence à la cellule Invisible par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | Prop.  *nom*  . Invisible où Prop.  *nom est*  le nom de ligne  <br/> |
   
Pour obtenir une référence à la cellule Invisible à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionProp** <br/> |
| Index de la ligne :  <br/> |**visRowProp** +   *i* où *i* = 0, 1, 2... |
| Index de la cellule :  <br/> |**visCustPropsInvis** <br/> |
   

