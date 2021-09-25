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
ms.openlocfilehash: 046ae26940da77297b1671af29ace286314dd730
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582616"
---
# <a name="invisible-cell-shape-data-section"></a>Invisible, cellule (section Shape Data)

Détermine si l’élément de données de forme est visible ou non dans la fenêtre **Données de forme**. 
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | Les données de forme ne sont pas visibles.  <br/> |
| FALSE  <br/> | L'élément de données de forme est visible.  <br/> |
   
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
| Index de la ligne :  <br/> |**visRowProp**  +   *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visCustPropsInvis** <br/> |
   

