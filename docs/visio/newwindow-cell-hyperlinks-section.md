---
title: NewWindow, cellule (section Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm695
ms.localizationpriority: medium
ms.assetid: 44995137-d241-937a-c097-0f9d79203cdf
description: Définit si le lien hypertexte doit être ouvert dans une nouvelle fenêtre.
ms.openlocfilehash: 0aac64fdae14d805b7131141e60da021ff6fa081
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63633882"
---
# <a name="newwindow-cell-hyperlinks-section"></a>NewWindow, cellule (section Hyperlinks)

Définit si le lien hypertexte doit être ouvert dans une nouvelle fenêtre.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | Ouvrez la page liée, le document ou le site web dans une nouvelle fenêtre. |
| FALSE  <br/> | Valeur par défaut. Le lien hypertexte n'est pas ouvert dans une nouvelle fenêtre. |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule NewWindow par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | Lien hypertexte.  *Nom*  . NewWindow où Lien hypertexte.  *Le nom*  est le nom de la ligne  <br/> |
   
Pour obtenir une référence à la cellule NewWindow à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionHyperlink** <br/> |
| **Index de la ligne :**  <br/> |**visRow1stHyperlink** +   *i* où *i* = 0, 1, 2, ... |
| **Index de la cellule :**  <br/> |**visHLinkNewWin** <br/> |
   

