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
ms.openlocfilehash: d00eb11ff1feffacf0d758bb25cdd56281e91327
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315203"
---
# <a name="gamma-cell-image-properties-section"></a>Gamma, cellule (section Image Properties)

Ajuste ou corrige l'intensité d'une image pour un périphérique de sortie spécifique tel qu'un moniteur ou un scanneur. La valeur par défaut est 1 (pas de correction).
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Gamma par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Gamma  <br/> |
   
Pour obtenir une référence à la cellule Gamma à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowImage** <br/> |
| Index de la cellule :  <br/> |**visImageGamma** <br/> |
   

