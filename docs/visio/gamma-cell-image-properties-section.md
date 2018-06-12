---
title: Gamma, cellule (section Image Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm410
localization_priority: Normal
ms.assetid: 3dcaee26-391c-0494-4380-890ee825dc47
description: Ajuste ou corrige l'intensité d'une image pour un périphérique de sortie spécifique tel qu'un moniteur ou un scanneur. La valeur par défaut est 1 (pas de correction).
ms.openlocfilehash: 060cb02aa8fd33e5a6c70a2c0236f16b9552aea0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788702"
---
# <a name="gamma-cell-image-properties-section"></a>Gamma, cellule (section Image Properties)

Ajuste ou corrige l'intensité d'une image pour un périphérique de sortie spécifique tel qu'un moniteur ou un scanneur. La valeur par défaut est 1 (pas de correction).
  
## <a name="remarks"></a>Note

Pour obtenir une référence à la cellule Gamma par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Gamma  <br/> |
   
Pour obtenir une référence à la cellule Gamma par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowImage** <br/> |
| Index de la cellule :  <br/> |**visImageGamma** <br/> |
   

