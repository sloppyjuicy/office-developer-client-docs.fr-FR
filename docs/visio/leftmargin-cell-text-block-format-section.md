---
title: LeftMargin, cellule (section Text Block Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251265
ms.localizationpriority: medium
ms.assetid: 47d84d7d-08a0-1934-d156-702da848e01c
description: Définit la distance entre le bord gauche du bloc de texte et le texte qui y figure. La valeur par défaut est de 2,5 mm. Cette valeur est indépendante de l'échelle du dessin. Si le dessin est mis à l'échelle, la marge gauche ne change pas.
ms.openlocfilehash: b4ded39a78c90e15a791f1db37564976899d44c6
ms.sourcegitcommit: 4164855836af53a068bbbc5b5d126f83ee83e324
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2022
ms.locfileid: "63426765"
---
# <a name="leftmargin-cell-text-block-format-section"></a>LeftMargin, cellule (section Text Block Format)

Définit la distance entre le bord gauche du bloc de texte et le texte qui y figure. La valeur par défaut est de 2,5 mm. Cette valeur est indépendante de l'échelle du dessin. Si le dessin est mis à l'échelle, la marge gauche ne change pas.
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule LeftMargin par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de la cellule :**  <br/> | LeftMargin  <br/> |
   
Pour obtenir une référence à la cellule LeftMargin à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowText** <br/> |
| **Index de la cellule :**  <br/> |**visTxtBlkLeftMargin** <br/> |
   

