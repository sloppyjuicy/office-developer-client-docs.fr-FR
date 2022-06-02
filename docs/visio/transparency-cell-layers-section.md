---
title: Transparency, cellule (section Layers)
description: Décrit les remarques de la cellule Transparency (section Layers), qui détermine le niveau de transparence d’une couleur de couche.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50130
ms.localizationpriority: medium
ms.assetid: 7382e2aa-5e18-19d2-88d8-c4a19a385106
ms.openlocfilehash: bcccd6492373203a8df72f8e914812c756db77a8
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65854083"
---
# <a name="transparency-cell-layers-section"></a>Transparency, cellule (section Layers)

Définit le niveau de transparence de la couleur d'un calque.
  
|**Valeur**|**Description**|
|:-----|:-----|
|0 - 100  <br/> |Représente le pourcentage de transparence. La valeur par défaut est 0 % (entièrement opaque). |
   
## <a name="remarks"></a>Remarques

Les valeurs sont arrondies au demi-point le plus proche. Une valeur de 100 % correspond à une transparence totale. Même si un calque dont la couleur est entièrement transparente apparaît identique sur la page de dessin à un calque dépourvu de couleur, il interagit avec les autres objets de la page de la même façon que s’il avait une transparence de 0 %. Vous pouvez également définir cette valeur à l’aide du curseur dans la boîte de dialogue **Propriétés des calques** (sous l’onglet **Accueil**, dans le groupe **Modification**, cliquez sur **Calques**, puis cliquez sur **Propriétés des calques**).
  
Pour obtenir une référence à la cellule Transparency par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de cellule :**  <br/> |Layers.ColorTrans[ *i*  ] où  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule Transparency par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionLayer** <br/> |
|**Index de la ligne :**  <br/> |**visRowLayer** +   *i* où *i* = 0, 1, 2... |
|**Index de la cellule :**  <br/> |**visLayerColorTrans** <br/> |
   

