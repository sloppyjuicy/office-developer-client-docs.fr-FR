---
title: LineGradientEnabled Cell (Gradient Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 276a661f-d14e-404a-a494-ae36601a8ce3
description: Détermine si un dégradé de trait est activé pour un trait ou la bordure d’une forme.
ms.openlocfilehash: 85ed79492195fb9902dad60e6b16fe7c655ee67a
ms.sourcegitcommit: 4164855836af53a068bbbc5b5d126f83ee83e324
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2022
ms.locfileid: "63427069"
---
# <a name="linegradientenabled-cell-gradient-properties-section"></a>LineGradientEnabled Cell (Gradient Properties Section)

Détermine si un dégradé de trait est activé pour un trait ou la bordure d’une forme. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Le dégradé est affiché sur le trait ou la bordure d’une forme. |
|FALSE  <br/> |Les dégradés ne sont pas affichés sur le trait ou la bordure d’une forme. |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **LineGradientEnabled** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | LineGradientEnabled  <br/> |
   
Pour obtenir une référence à la cellule **LineGradientEnabled** à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowGradientProperties** <br/> |
| **Index de la cellule :**  <br/> |**visLineGradientEnabled** <br/> |
   

