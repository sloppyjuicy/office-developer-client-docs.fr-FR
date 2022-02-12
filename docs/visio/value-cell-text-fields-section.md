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
ms.openlocfilehash: d2f7487963c48da8be23fe859f515f02cdf328b1
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62779027"
---
# <a name="value-cell-text-fields-section"></a>Value, cellule (section Text Fields)

Contient la fonction d'un champ.
  
## <a name="remarks"></a>Remarques

Vous pouvez définir la valeur de cette cellule au moyen de la boîte de dialogue **Champ** (sous l’onglet **Insertion**, dans le groupe **Texte**, cliquez sur **Champ**).
  
Pour obtenir une référence à la cellule Value par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |Fields.Value[ *i*  ] où  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule Value par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionTextField** <br/> |
|Index de la ligne :  <br/> |**visRowField** +   *i* où *i* = 0, 1, 2... |
|Index de la cellule :  <br/> |**visFieldCell** <br/> |
   

