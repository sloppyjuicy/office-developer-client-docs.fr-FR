---
title: ShdwObliqueAngle, cellule (section Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033178
ms.localizationpriority: medium
ms.assetid: 2e0b9754-3e3b-3a26-4e1a-e09102055c20
description: Contient une valeur indiquant l'angle de la direction oblique lors de l'application du type d'ombre par défaut de la page.
ms.openlocfilehash: 2b8949f519c04206a224ef91e847e73e3d5f0757
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63626121"
---
# <a name="shdwobliqueangle-cell-page-properties-section"></a>ShdwObliqueAngle, cellule (section Page Properties)

Contient une valeur indiquant l'angle de la direction oblique lors de l'application du type d'ombre par défaut de la page.
  
## <a name="remarks"></a>Remarques

Une valeur de zéro (0) dans cette cellule indique que la direction de l'angle est verticale et mesurée dans le sens des aiguilles d'une montre.
  
 L’angle décrit dans cette cellule est utilisé chaque fois que la cellule ShapeShdwType (le type d’ombre d’une forme sur la page) est définie sur Page Default (**visFSTPageDefault** ), et que le type d’ombre est oblique. Le type d'ombre par défaut de la page est défini dans la cellule ShdwType. 
  
Pour définir ce comportement pour une forme individuelle, utilisez la cellule ShapeShdwObliqueAngle dans la section Fill Format.
  
Pour obtenir une référence à la cellule ShdwObliqueAngle par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | ShdwObliqueAngle  <br/> |
   
Pour obtenir une référence à la cellule ShdwObliqueAngle par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowPage** <br/> |
| **Index de la cellule :**  <br/> |**visPageShdwObliqueAngle** <br/> |
   

