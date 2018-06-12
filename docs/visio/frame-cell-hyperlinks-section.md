---
title: Frame, cellule (section Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm405
localization_priority: Normal
ms.assetid: f71d8737-92ef-1124-ba4a-b7e17305bd0a
description: Représente le nom d'un cadre à prendre comme destination lorsque l'application est ouverte comme document actif dans une application conteneur. La valeur par défaut est une chaîne vide.
ms.openlocfilehash: b94e5efd4a3fdf53e01f7518252852214a72c766
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788699"
---
# <a name="frame-cell-hyperlinks-section"></a>Frame, cellule (section Hyperlinks)

Représente le nom d'un cadre à prendre comme destination lorsque l'application est ouverte comme document actif dans une application conteneur. La valeur par défaut est une chaîne vide.
  
## <a name="remarks"></a>Note

Pour obtenir une référence à la cellule Frame par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Lien hypertexte.  *nom* . Encadrer où un lien hypertexte.  *Name* est le nom de ligne  <br/> |
   
Pour obtenir une référence à la cellule Frame par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionHyperlink** <br/> |
| Index de la ligne :  <br/> |**visRow1stHyperlink** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visHLinkFrame** <br/> |
   

