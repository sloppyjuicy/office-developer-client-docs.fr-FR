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
description: Contient la valeur de l’élément de données de forme entré dans la boîte de dialogue Définir les données de forme.
ms.openlocfilehash: 5b373149360167585fc5a143ce9458703e219045
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790005"
---
# <a name="value-cell-shape-data-section"></a>Value, cellule (section Shape Data)

Contient la valeur de l’élément de données de forme entré dans la boîte de dialogue **Définir les données de forme** . 
  
## <a name="remarks"></a>Remarques

Les formules entrées dans cette cellule sont remplacées par les valeurs entrées dans la boîte de dialogue **Définir les données de forme** . Cela est vrai même si vous utilisez la fonction GUARD pour protéger la formule. 
  
Pour obtenir une référence à la cellule Value par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Propriétés.  *Nom* . Valeur de propriétés où.  *Name* est le nom de ligne  <br/> |
   
Pour obtenir une référence à la cellule Value par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionProp** <br/> |
| Index de la ligne :  <br/> |**visRowProp** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visCustPropsValue** <br/> |
   

