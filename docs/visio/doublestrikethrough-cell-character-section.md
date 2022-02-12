---
title: DoubleStrikethrough, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033762
ms.localizationpriority: medium
ms.assetid: c48a77e1-ea3c-7a6d-8c05-f9e0cb434cda
description: Détermine si du texte est barré double.
ms.openlocfilehash: 226f39552d0eda012023cf9d841aae9bead6a40a
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62774369"
---
# <a name="doublestrikethrough-cell-character-section"></a>DoubleStrikethrough, cellule (section Character)

Détermine si du texte est barré double.
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule DoubleStrikethrough par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Char.DoubleStrikethrough[  *i*  ] où  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule DoubleStrikethrough à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionCharacter** <br/> |
| Index de la ligne :  <br/> |**visRowCharacter** +   *i* où *i* = 0, 1, 2... |
| Index de la cellule :  <br/> |**visCharacterDoubleStrikethrough** <br/> |
   

