---
title: ClippingPath, cellule (Section Foreign Image Info)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ec70417-5b23-45af-95a0-1b26f6791699
description: Contient une référence à la géométrie d’une image délimitée par le chemin d’accès.
ms.openlocfilehash: 9f1c159e303c1d7bc3467c36756a422a3f325c7b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788254"
---
# <a name="clippingpath-cell-foreign-image-info-section"></a>ClippingPath, cellule (Section Foreign Image Info)

Contient une référence à la géométrie d’une image délimitée par le chemin d’accès. 
  
## <a name="remarks"></a>Remarques

Si la cellule **ClippingPath** pointe vers un chemin d’accès valide, l’image est découpée afin que l’image s’affiche dans le chemin d’accès. Si la cellule **ClippingPath** est vide ou contient une entrée non valide, l’image est rendue par un élément rectangulaire, en utilisant les valeurs à l’échelle et de décalage. 
  
> [!NOTE]
> Uniquement les chemins d’accès définis par une section [Geometry](geometry-section.md) dans la feuille ShapeSheet de l’image sont des entrées valides pour la cellule **ClippingPath** . Références entre différentes feuilles ne peut pas être utilisés pour définir un masque d’image. 
  
Pour obtenir une référence à la cellule **ClippingPath** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | ClippingPath  <br/> |
   
Pour obtenir une référence à la cellule **ClippingPath** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowForeign** <br/> |
| Index de la cellule :  <br/> |**visFrgnImgClippingPath** <br/> |
   
## <a name="example"></a>Exemple

Vous pouvez modifier la forme de délimitation d’une image à un ovale en procédant comme suit :
  
- Insérez l’image sur la zone de dessin.
    
- Cliquez sur l’image, puis sélectionnez **Afficher la feuille ShapeSheet**.
    
- Avec le bouton droit n’importe où dans la feuille ShapeSheet et sélectionnez **Insérer une Section**.
    
- Dans la boîte de dialogue **Insérer une Section** , sélectionnez la **géométrie** , puis sur **OK**.
    
- Dans la section Geometry nouveaux (par exemple, « Geometry2 »), supprimez tout sauf une ligne.
    
- Avec le bouton droit de la ligne restante, puis sur **Modifier le Type de ligne**.
    
- Dans la boîte de dialogue **Modifier le Type de ligne** , sélectionnez **Ellipse** , puis cliquez sur **OK**.
    
- Dans la section **Foreign Image** , définir la formule pour la cellule **ClippingPath** à `="Geometry2.Path"` , puis acceptez la formule. 
    

