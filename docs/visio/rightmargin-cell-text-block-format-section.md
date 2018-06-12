---
title: RightMargin, cellule (section Text Block Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251266
localization_priority: Normal
ms.assetid: bc8f5469-e79f-4a68-73cb-d11c938353a4
description: Définit la distance séparant le bord droit du bloc de texte du texte qui y figure. La valeur par défaut est 2,54 mm.
ms.openlocfilehash: 57fdb320395a9a6562983a0148b37c4a70a9a9b6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789482"
---
# <a name="rightmargin-cell-text-block-format-section"></a>RightMargin, cellule (section Text Block Format)

Définit la distance séparant le bord droit du bloc de texte du texte qui y figure. La valeur par défaut est 2,54 mm.
  
## <a name="remarks"></a>Note

Cette valeur est indépendante de l'échelle du dessin. Si le dessin est mis à l'échelle, la marge droite ne change pas.
  
Pour obtenir une référence à la cellule RightMargin par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | RightMargin  <br/> |
   
Pour obtenir une référence à la cellule RightMargin par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowText** <br/> |
| Index de la cellule :  <br/> |**visTxtBlkRightMargin** <br/> |
   

