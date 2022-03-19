---
title: RightMargin, cellule (section Text Block Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251266
ms.localizationpriority: medium
ms.assetid: bc8f5469-e79f-4a68-73cb-d11c938353a4
description: Définit la distance séparant le bord droit du bloc de texte du texte qui y figure. La valeur par défaut est 2,54 mm.
ms.openlocfilehash: b433e006747929cf071e7e00e478850e5fa77750
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63634771"
---
# <a name="rightmargin-cell-text-block-format-section"></a>RightMargin, cellule (section Text Block Format)

Définit la distance séparant le bord droit du bloc de texte du texte qui y figure. La valeur par défaut est 2,54 mm.
  
## <a name="remarks"></a>Remarques

Cette valeur est indépendante de l'échelle du dessin. Si le dessin est mis à l'échelle, la marge droite ne change pas.
  
Pour obtenir une référence à la cellule RightMargin par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de la cellule :**  <br/> | RightMargin  <br/> |
   
Pour obtenir une référence à la cellule RightMargin à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowText** <br/> |
| **Index de la cellule :**  <br/> |**visTxtBlkRightMargin** <br/> |
   

