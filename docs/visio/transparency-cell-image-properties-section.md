---
title: Transparency, cellule (section Image Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm51095
localization_priority: Normal
ms.assetid: 5b265356-1602-4241-fbe1-4d5a55392a52
description: Définit le niveau de transparence de la couleur d'un calque.
ms.openlocfilehash: 5537cbdcd49c66f3bc28a58051f6e2888a290cd3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789922"
---
# <a name="transparency-cell-image-properties-section"></a>Transparency, cellule (section Image Properties)

Définit le niveau de transparence de la couleur d'un calque.
  
|**Valeur**|**Description**|
|:-----|:-----|
|0 - 100  <br/> |Représente le pourcentage de transparence. La valeur par défaut est 0 % (entièrement opaque).  <br/> |
   
## <a name="remarks"></a>Remarques

Les valeurs sont arrondies au pourcentage le plus proche. Une valeur de 100 % est complètement transparente. Bien qu’un calque dont la couleur transparente complètement la même page de dessin s’affiche en tant que couche qui n’a aucune couleur, il interagit avec d’autres objets dans la page de la même manière que si sa transparence ont été 0 %. Vous pouvez également définir cette valeur à l’aide du curseur dans la boîte de dialogue **Propriétés des calques** (sous l’onglet **accueil** , dans le groupe **modification** , cliquez sur **calques**, puis cliquez sur **Propriétés des calques**).
  
Pour obtenir une référence à la cellule Transparency par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |Transparency  <br/> |
   
Pour obtenir une référence à la cellule Transparency par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowImage** <br/> |
|Index de la cellule :  <br/> |**visImageTransparency** <br/> |
   

