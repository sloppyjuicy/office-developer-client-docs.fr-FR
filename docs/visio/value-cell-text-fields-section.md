---
title: Value, cellule (section Text Fields)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1095
localization_priority: Normal
ms.assetid: 3ca662c8-1ce4-89a9-3264-1ba533fcd444
description: Contient la fonction d'un champ.
ms.openlocfilehash: 9bce4cbb1b3955f749cefa18130c6b01fe61244e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789995"
---
# <a name="value-cell-text-fields-section"></a>Value, cellule (section Text Fields)

Contient la fonction d'un champ.
  
## <a name="remarks"></a>Remarques

Vous pouvez définir la valeur de cette cellule à l’aide de la boîte de dialogue **champ** (sous l’onglet **Insertion** , dans le groupe **texte** , cliquez sur **champ**).
  
Pour obtenir une référence à la cellule Value par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |Fields.Value [ *i* ] où *i* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule Value par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionTextField** <br/> |
|Index de la ligne :  <br/> |**visRowField** +  *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visFieldCell** <br/> |
   

