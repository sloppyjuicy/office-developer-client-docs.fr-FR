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
ms.openlocfilehash: d660453da25e6c9b3f3be3957d2f8253f141d5f7
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63627941"
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
  
||Valeur |
|:-----|:-----|
| **Nom de la cellule :**  <br/> | TextDirection  <br/> |
   
Pour obtenir une référence à la cellule TextDirection par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowText** <br/> |
| **Index de la cellule :**  <br/> |**visTxtBlkDirection** <br/> |
   

