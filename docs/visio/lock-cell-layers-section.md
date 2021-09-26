---
title: Lock, cellule (section Layers)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm590
ms.localizationpriority: medium
ms.assetid: 47bb268f-acdd-7369-716c-bd51a32b8a49
description: Indique si les formes appartenant au calque sont verrouillées en sélection ou en modification.
ms.openlocfilehash: 62ae9a41a2ba38b35469026525a6549cd72ba467
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612504"
---
# <a name="lock-cell-layers-section"></a>Lock, cellule (section Layers)

Indique si les formes appartenant au calque sont verrouillées en sélection ou en modification.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Les formes sont verrouillées.  <br/> |
|FALSE  <br/> |Aucune forme n'est verrouillée.  <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir cette valeur en activant la case à cocher **Verrouiller** dans la boîte de dialogue **Propriétés des calques**(sous l’onglet **Accueil**, dans le groupe **Modification**, cliquez sur **Calques**, puis cliquez sur **Propriétés des calques**).
  
Pour obtenir une référence à la cellule Lock par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |Layers.Locked[ *i*  ] où  *i*  = <1>, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule Lock à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionLayer** <br/> |
|Index de la ligne :  <br/> |**visRowLayer**  +   *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visLayerLock** <br/> |
   

