---
title: Invisible, cellule (section Shape Data)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251341
localization_priority: Normal
ms.assetid: 5f368c2e-2a40-38ee-3568-ed5c57633345
description: Spécifie si l’élément de données de forme est visible dans la fenêtre données de forme.
ms.openlocfilehash: 2cd3fcad5db7b1752c55055354f1ec842bff4899
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788838"
---
# <a name="invisible-cell-shape-data-section"></a>Invisible, cellule (section Shape Data)

Spécifie si l’élément de données de forme est visible dans la fenêtre **Données de forme** . 
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | Les données de forme ne sont pas visibles.  <br/> |
| FALSE  <br/> | L'élément de données de forme est visible.  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur de cette cellule correspond à la case à cocher **masqué** dans la boîte de dialogue **Définir les données de forme** (avec le bouton droit de la forme, pointez sur **données**, puis cliquez sur **Définir les données de forme**).
  
Pour obtenir une référence à la cellule Invisible par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Propriétés.  *nom* . Where invisible de propriétés.  *Name* est le nom de ligne  <br/> |
   
Pour obtenir une référence à la cellule Invisible par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionProp** <br/> |
| Index de la ligne :  <br/> |**visRowProp** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visCustPropsInvis** <br/> |
   

