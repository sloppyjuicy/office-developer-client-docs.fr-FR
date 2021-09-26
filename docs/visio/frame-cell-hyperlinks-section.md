---
title: Frame, cellule (section Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm405
ms.localizationpriority: medium
ms.assetid: f71d8737-92ef-1124-ba4a-b7e17305bd0a
description: Représente le nom d'un cadre à prendre comme destination lorsque l'application est ouverte comme document actif dans une application conteneur. La valeur par défaut est une chaîne vide.
ms.openlocfilehash: 436a95ac60b01d951e84e6deb5d1a03887c82b47
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598590"
---
# <a name="frame-cell-hyperlinks-section"></a>Frame, cellule (section Hyperlinks)

Représente le nom d'un cadre à prendre comme destination lorsque l'application est ouverte comme document actif dans une application conteneur. La valeur par défaut est une chaîne vide.
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Frame par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Lien hypertexte.  *nom*  . Cadre où lien hypertexte.  *nom est*  le nom de ligne  <br/> |
   
Pour obtenir une référence à la cellule Frame à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionHyperlink** <br/> |
| Index de la ligne :  <br/> |**visRow1stHyperlink**  +   *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visHLinkFrame** <br/> |
   

