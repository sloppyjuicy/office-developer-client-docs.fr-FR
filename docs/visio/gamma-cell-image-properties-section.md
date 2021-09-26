---
title: Gamma, cellule (section Image Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm410
ms.localizationpriority: medium
ms.assetid: 3dcaee26-391c-0494-4380-890ee825dc47
description: Ajuste ou corrige l'intensité d'une image pour un périphérique de sortie spécifique tel qu'un moniteur ou un scanneur. La valeur par défaut est 1 (pas de correction).
ms.openlocfilehash: 211d16b25839ed182dbe785f38a6bbe95633c953
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618965"
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
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowImage** <br/> |
| Index de la cellule :  <br/> |**visImageGamma** <br/> |
   

