---
title: NoShow, cellule (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm735
localization_priority: Normal
ms.assetid: 831075ff-2875-b598-00bb-eb8481fee57b
description: Indique si un chemin est affiché sur la page de dessin.
ms.openlocfilehash: ad4d9cf1aa3e541f512bc09ffc38cf03204b3c94
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789203"
---
# <a name="noshow-cell-geometry-section"></a>NoShow, cellule (section Geometry)

Indique si un chemin est affiché sur la page de dessin.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | Le trait et le remplissage du chemin représentés par cette section sont masqués.  <br/> |
| FALSE  <br/> | Le trait et le remplissage du chemin sont affichés.  <br/> |
   
## <a name="remarks"></a>Note

Pour obtenir une référence à la cellule NoShow par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Géométrie *i* . NoShow où *i* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule NoShow par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionFirstComponent** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la ligne :  <br/> |**visRowComponent** <br/> |
| Index de la cellule :  <br/> |**visCompNoShow** <br/> |
   

