---
title: ExtraInfo, cellule (section Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm360
localization_priority: Normal
ms.assetid: 55834445-8619-f79a-aea0-0f6a1780e016
description: Représente une chaîne qui transmet les informations à utiliser dans la résolution d’une URL, comme les coordonnées d’une image interactive. Par exemple, dans la cellule ExtraInfo, x = 41&amp;y = 7specifies les coordonnées d’une image interactive.
ms.openlocfilehash: aa035d5ec863cd8045063af970efa26b53683793
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788601"
---
# <a name="extrainfo-cell-hyperlinks-section"></a>ExtraInfo, cellule (section Hyperlinks)

Représente une chaîne qui transmet les informations à utiliser dans la résolution d’une URL, comme les coordonnées d’une image interactive. Par exemple, dans la cellule ExtraInfo, « x = 41&amp;y = 7 » indique les coordonnées d’une image interactive.
  
## <a name="remarks"></a>Remarques

Les cellules Event ne sont évaluées que lorsque l'événement se produit, et non lors de l'entrée de la formule.
  
Pour obtenir une référence à la cellule ExtraInfo par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Lien hypertexte.  *nom* . ExtraInfo où un lien hypertexte.  *Name* est le nom de ligne  <br/> |
   
Pour obtenir une référence à la cellule ExtraInfo par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionHyperlink** <br/> |
| Index de la ligne :  <br/> |**visRow1stHyperlink** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visHLinkExtraInfo** <br/> |
   

