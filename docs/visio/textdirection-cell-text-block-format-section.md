---
title: TextDirection, cellule (section Text Block Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm995
localization_priority: Normal
ms.assetid: 1df3a50e-7ea5-9244-1286-c1d00c217a9a
description: Détermine le sens des caractères dans un bloc de texte.
ms.openlocfilehash: c238b6b2a47c968809869f8eb3e38b6f0db1dcad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789890"
---
# <a name="textdirection-cell-text-block-format-section"></a>TextDirection, cellule (section Text Block Format)

Détermine le sens des caractères dans un bloc de texte.
  
|**Valeur**|**Direction**|**Constante d’Automation**|
|:-----|:-----|:-----|
| 0  <br/> | Horizontal  <br/> |**visTxtBlkLeftToRight** <br/> |
| 1  <br/> | Vertical  <br/> |**visTxtBlkTopToBottom** <br/> |
   
## <a name="remarks"></a>Note

Dans la version japonaise 5.0 de Visio, la valeur de cette cellule était stockée dans la cellule VerticalText de la section Miscellaneous.
  
Pour obtenir une référence à la cellule TextDirection par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | TextDirection  <br/> |
   
Pour obtenir une référence à la cellule TextDirection par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowText** <br/> |
| Index de la cellule :  <br/> |**visTxtBlkDirection** <br/> |
   

