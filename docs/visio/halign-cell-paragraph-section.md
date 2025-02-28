---
title: HAlign, cellule (section Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm425
ms.localizationpriority: medium
ms.assetid: a8d6b622-60b3-e43f-b6a1-55db561204ed
description: Détermine l'alignement horizontal du texte dans le bloc de texte de la forme.
ms.openlocfilehash: 514391217f4cd5885e6afbe26c898a2e1d60eeb6
ms.sourcegitcommit: 7b410a51d1e8c97e9cce8d4aa75074162b7d9485
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/12/2022
ms.locfileid: "63448726"
---
# <a name="halign-cell-paragraph-section"></a>HAlign, cellule (section Paragraph)

Détermine l'alignement horizontal du texte dans le bloc de texte de la forme.
  
|**Valeur**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
| 0  <br/> | Alignement à gauche  <br/> |**visHorzLeft** <br/> |
| 1  <br/> | Centre  <br/> |**visHorzCenter** <br/> |
| 2  <br/> | Alignement à droite  <br/> |**visHorzRight** <br/> |
| 3  <br/> | Justifier  <br/> |**visHorzJustify** <br/> |
| 4  <br/> | Justification forcée  <br/> |**visHorzForce** <br/> |
   
## <a name="remarks"></a>Remarques

La justification ajoute des espaces entre les mots de toutes les lignes, à l'exception de la dernière ligne du paragraphe, pour aligner les côtés gauche et droit du texte sur les marges.
  
La justification forcée aligne toutes les lignes du paragraphe, y compris la dernière.
  
Pour obtenir une référence à la cellule HAlign par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | Para.HorzAlign[  *i*  ] where  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule HAlign à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionParagraph** <br/> |
| **Index de la ligne :**  <br/> |**visRowParagraph** +   *i* où *i* = 0, 1, 2... |
| **Index de la cellule :**  <br/> |**visHorzAlign** <br/> |
   

