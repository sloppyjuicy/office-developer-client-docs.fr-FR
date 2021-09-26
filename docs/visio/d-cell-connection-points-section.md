---
title: D, cellule (section Connection Points)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm205
ms.localizationpriority: medium
ms.assetid: 28b18e8d-fecf-a798-813e-c1a310002244
description: Cellule de montage utilisable pour entrer ou tester des formules.
ms.openlocfilehash: 3db35be72fb80c7f08a751e961535403b5ceff8f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613015"
---
# <a name="d-cell-connection-points-section"></a>D, cellule (section Connection Points)

Cellule de montage utilisable pour entrer ou tester des formules.
  
## <a name="remarks"></a>Remarques

Pour accéder à la cellule D, cliquez avec le bouton droit de la souris sur une ligne, puis cliquez sur **Modifier le type de ligne** dans le menu contextuel. 
  
Pour obtenir une référence à la cellule D par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Connections.D[  *i*  ] où  *i*  = <1>, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule D à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionConnectionPts** <br/> |
| Index de la ligne :  <br/> |**visRowConnectionPts**  +   *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visCnnctD** <br/> |
   

