---
title: NewWindow, cellule (section Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm695
localization_priority: Normal
ms.assetid: 44995137-d241-937a-c097-0f9d79203cdf
description: Définit si le lien hypertexte doit être ouvert dans une nouvelle fenêtre.
ms.openlocfilehash: 0f9d1e4b1294dea3f211c8d0d69ffc49b6180066
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342230"
---
# <a name="newwindow-cell-hyperlinks-section"></a>NewWindow, cellule (section Hyperlinks)

Définit si le lien hypertexte doit être ouvert dans une nouvelle fenêtre.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | Ouvrez la page liée, le document ou le site web dans une nouvelle fenêtre.  <br/> |
| FALSE  <br/> | Valeur par défaut. Le lien hypertexte n'est pas ouvert dans une nouvelle fenêtre.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule NewWindow par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Lien hypertexte.  *Nom*  . NewWindow où Lien hypertexte.  *Le nom*  est le nom de la ligne  <br/> |
   
Pour obtenir une référence à la cellule NewWindow à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionHyperlink** <br/> |
| Index de la ligne :  <br/> |**visRow1stHyperlink**  +   *i* où *i* = 0, 1, 2, ...  <br/> |
| Index de la cellule :  <br/> |**visHLinkNewWin** <br/> |
   

