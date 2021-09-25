---
title: TextDirection, cellule (section Text Block Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm995
ms.localizationpriority: medium
ms.assetid: 1df3a50e-7ea5-9244-1286-c1d00c217a9a
description: Détermine le sens des caractères dans un bloc de texte.
ms.openlocfilehash: d70cf6152fcb3e7ffbda69f6a6e6aaf758074fd1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59553689"
---
# <a name="textdirection-cell-text-block-format-section"></a>TextDirection, cellule (section Text Block Format)

Détermine le sens des caractères dans un bloc de texte.
  
|**Valeur**|**Direction**|**Constante d'automation**|
|:-----|:-----|:-----|
| 0  <br/> | Horizontal  <br/> |**visTxtBlkLeftToRight** <br/> |
| 1  <br/> | Vertical  <br/> |**visTxtBlkTopToBottom** <br/> |
   
## <a name="remarks"></a>Remarques

Dans la version japonaise 5.0 de Visio, la valeur de cette cellule était stockée dans la cellule VerticalText de la section Miscellaneous.
  
Pour obtenir une référence à la cellule TextDirection par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | TextDirection  <br/> |
   
Pour obtenir une référence à la cellule TextDirection par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowText** <br/> |
| Index de la cellule :  <br/> |**visTxtBlkDirection** <br/> |
   

