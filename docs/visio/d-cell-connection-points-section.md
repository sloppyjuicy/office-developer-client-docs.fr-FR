---
title: D, cellule (section Connection Points)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm205
localization_priority: Normal
ms.assetid: 28b18e8d-fecf-a798-813e-c1a310002244
description: Cellule de montage utilisable pour entrer ou tester des formules.
ms.openlocfilehash: 21c81c7a0a64c3016d8cff3b33d83ce785dc24eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788396"
---
# <a name="d-cell-connection-points-section"></a>D, cellule (section Connection Points)

Cellule de montage utilisable pour entrer ou tester des formules.
  
## <a name="remarks"></a>Remarques

Pour accéder à la cellule D, cliquez sur une ligne, puis cliquez sur **Modifier le Type de ligne** dans le menu contextuel. 
  
Pour obtenir une référence à la cellule D par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Connections.D [ *i* ] où *i* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule D par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionConnectionPts** <br/> |
| Index de la ligne :  <br/> |**visRowConnectionPts** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visCnnctD** <br/> |
   

