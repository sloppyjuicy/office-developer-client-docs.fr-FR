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
ms.openlocfilehash: b4d927e1970e994047df3cb89afa7799a825511d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789165"
---
# <a name="newwindow-cell-hyperlinks-section"></a>NewWindow, cellule (section Hyperlinks)

Définit si le lien hypertexte doit être ouvert dans une nouvelle fenêtre.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | La page, le document ou le site Web est ouvert dans une nouvelle fenêtre.  <br/> |
| FALSE  <br/> | Valeur par défaut. Le lien hypertexte n'est pas ouvert dans une nouvelle fenêtre.  <br/> |
   
## <a name="remarks"></a>Note

Pour obtenir une référence à la cellule NewWindow par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Lien hypertexte.  *Nom* . NewWindow où un lien hypertexte.  *Name* est le nom de ligne  <br/> |
   
Pour obtenir une référence à la cellule NewWindow par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionHyperlink** <br/> |
| Index de la ligne :  <br/> |**visRow1stHyperlink** +  *i* où *i* = 0, 1, 2,...  <br/> |
| Index de la cellule :  <br/> |**visHLinkNewWin** <br/> |
   

