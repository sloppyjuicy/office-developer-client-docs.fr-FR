---
title: Value, cellule (section Text Fields)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1095
ms.localizationpriority: medium
ms.assetid: 3ca662c8-1ce4-89a9-3264-1ba533fcd444
description: Contient la fonction d'un champ.
ms.openlocfilehash: b81a384ac5a0327fb1725c2297389e334907579b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59569838"
---
# <a name="value-cell-text-fields-section"></a>Value, cellule (section Text Fields)

Contient la fonction d'un champ.
  
## <a name="remarks"></a>Remarques

Vous pouvez définir la valeur de cette cellule au moyen de la boîte de dialogue **Champ** (sous l’onglet **Insertion**, dans le groupe **Texte**, cliquez sur **Champ**).
  
Pour obtenir une référence à la cellule Value par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |Fields.Value[ *i*  ] où  *i*  = <1>, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule Value par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionTextField** <br/> |
|Index de la ligne :  <br/> |**visRowField**  +   *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visFieldCell** <br/> |
   

