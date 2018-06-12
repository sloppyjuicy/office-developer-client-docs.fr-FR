---
title: Active, cellule (section Layers)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm10
localization_priority: Normal
ms.assetid: 4c8e366f-9e9b-30ea-a89f-57c8d7a1168e
description: Détermine si le calque est actif. Les formes sans calque pré-attribué sont affectées aux calques actifs lorsque vous les faites glisser sur la page de dessin.
ms.openlocfilehash: 81d3ec083e207a927c46dda99e2b7f42c0a7bd8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788004"
---
# <a name="active-cell-layers-section"></a>Active, cellule (section Layers)

Détermine si le calque est actif. Les formes sans calque pré-attribué sont affectées aux calques actifs lorsque vous les faites glisser sur la page de dessin.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Le calque est actif.  <br/> |
|FALSE  <br/> |Calque n’est pas actif.  <br/> |
   
## <a name="remarks"></a>Note

La valeur de cette cellule correspond au paramètre **actif** de la boîte de dialogue **Propriétés des calques** (dans le groupe **modification** , sous l’onglet **accueil** , cliquez sur **calques**, puis cliquez sur **Propriétés des calques**).
  
Pour obtenir une référence à la cellule Active par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |Layers.Active [ *i* ] où *i* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule Active par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionLayer** <br/> |
|Index de la ligne :  <br/> |**visRowLayer** +  *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visLayerActive** <br/> |
   

