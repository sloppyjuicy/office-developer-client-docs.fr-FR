---
title: Transparency, cellule (section Layers)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50130
localization_priority: Normal
ms.assetid: 7382e2aa-5e18-19d2-88d8-c4a19a385106
description: Définit le niveau de transparence de la couleur d'un calque.
ms.openlocfilehash: 7c205612436e7731f268e17c851616beebf809dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789928"
---
# <a name="transparency-cell-layers-section"></a>Transparency, cellule (section Layers)

Définit le niveau de transparence de la couleur d'un calque.
  
|**Valeur**|**Description**|
|:-----|:-----|
|0 - 100  <br/> |Représente le pourcentage de transparence. La valeur par défaut est 0 % (entièrement opaque).  <br/> |
   
## <a name="remarks"></a>Remarques

Les valeurs sont arrondies au pourcentage le plus proche. Une valeur de 100 % est complètement transparente. Bien qu’un calque dont la couleur transparente complètement la même page de dessin s’affiche en tant que couche qui n’a aucune couleur, il interagit avec d’autres objets dans la page de la même manière que si sa transparence ont été 0 %. Vous pouvez également définir cette valeur à l’aide du curseur dans la boîte de dialogue **Propriétés des calques** (sous l’onglet **accueil** , dans le groupe **modification** , cliquez sur **calques**, puis cliquez sur **Propriétés des calques**).
  
Pour obtenir une référence à la cellule Transparency par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |Layers.ColorTrans [ *i* ] où *i* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule Transparency par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionLayer** <br/> |
|Index de la ligne :  <br/> |**visRowLayer** +  *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visLayerColorTrans** <br/> |
   

