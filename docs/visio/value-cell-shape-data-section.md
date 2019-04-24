---
title: Value, cellule (section Shape Data)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1090
localization_priority: Normal
ms.assetid: fd42a6ce-f621-4e9e-aba3-23a1b87a5651
description: Contient la valeur de l’élément de données de forme telle qu’elle est saisie dans la boîte de dialogue Définir les données de forme.
ms.openlocfilehash: 40d9e7fdd92ac8fa800a146ea45bbcd002ace87b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355971"
---
# <a name="value-cell-shape-data-section"></a>Value, cellule (section Shape Data)

Contient la valeur de l’élément de données de forme telle qu’elle est saisie dans la boîte de dialogue **Définir les données de forme**. 
  
## <a name="remarks"></a>Remarques

Les formules entrées dans cette cellule sont remplacées par les valeurs entrées dans la boîte de dialogue **Définir les données de forme**. Cette règle est d’application même si vous utilisez la fonction GUARD pour protéger la formule. 
  
Pour obtenir une référence à la cellule Value par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | Hélice.  *Nom* . Valeur où prop.  *Name* est le nom de la ligne  <br/> |
   
Pour obtenir une référence à la cellule Value par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionProp** <br/> |
| Index de la ligne :  <br/> |**visRowProp** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visCustPropsValue** <br/> |
   

