---
title: Value, cellule (section Shape Data)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1090
ms.localizationpriority: medium
ms.assetid: fd42a6ce-f621-4e9e-aba3-23a1b87a5651
description: Contient la valeur de l’élément de données de forme telle qu’elle est saisie dans la boîte de dialogue Définir les données de forme.
ms.openlocfilehash: b39f9218405685de041d49dc7fdcd27fa634d833
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62788709"
---
# <a name="value-cell-shape-data-section"></a>Value, cellule (section Shape Data)

Contient la valeur de l’élément de données de forme telle qu’elle est saisie dans la boîte de dialogue **Définir les données de forme**. 
  
## <a name="remarks"></a>Remarques

Les formules entrées dans cette cellule sont remplacées par les valeurs entrées dans la boîte de dialogue **Définir les données de forme**. Cette règle est d’application même si vous utilisez la fonction GUARD pour protéger la formule. 
  
Pour obtenir une référence à la cellule Value par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | Prop.  *Nom*  . Valeur où Prop.  *Le nom*  est le nom de la ligne  <br/> |
   
Pour obtenir une référence à la cellule Value par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionProp** <br/> |
| Index de la ligne :  <br/> |**visRowProp** +   *i* où *i* = 0, 1, 2... |
| Index de la cellule :  <br/> |**visCustPropsValue** <br/> |
   

