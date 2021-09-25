---
title: NoShow, cellule (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm735
ms.localizationpriority: medium
ms.assetid: 831075ff-2875-b598-00bb-eb8481fee57b
description: Indique si un chemin est affiché sur la page de dessin.
ms.openlocfilehash: 7d545fe9526cad6aca87998f7a62cfff0f9a314d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577807"
---
# <a name="noshow-cell-geometry-section"></a>NoShow, cellule (section Geometry)

Indique si un chemin est affiché sur la page de dessin.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | Le trait et le remplissage du chemin représentés par cette section sont masqués.  <br/> |
| FALSE  <br/> | Le trait et le remplissage du chemin sont affichés.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule NoShow par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Geometry  *i*  . NoShow où  *i*  = <1>, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule NoShow à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionFirstComponent**  +   *i* où *i* = 0, 1, 2...  <br/> |
| Index de la ligne :  <br/> |**visRowComponent** <br/> |
| Index de la cellule :  <br/> |**visCompNoShow** <br/> |
   

