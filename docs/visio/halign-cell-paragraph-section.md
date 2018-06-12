---
title: HAlign, cellule (section Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm425
localization_priority: Normal
ms.assetid: a8d6b622-60b3-e43f-b6a1-55db561204ed
description: Détermine l'alignement horizontal du texte dans le bloc de texte de la forme.
ms.openlocfilehash: 224e495e8aea70c418a0ab7f5a7d56975d9868e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788762"
---
# <a name="halign-cell-paragraph-section"></a>HAlign, cellule (section Paragraph)

Détermine l'alignement horizontal du texte dans le bloc de texte de la forme.
  
|**Valeur**|**Description**|**Constante d’Automation**|
|:-----|:-----|:-----|
| 0  <br/> | Alignement à gauche  <br/> |**visHorzLeft** <br/> |
| 1  <br/> | Au centre  <br/> |**visHorzCenter** <br/> |
| 2  <br/> | Alignement à droite  <br/> |**visHorzRight** <br/> |
| 3  <br/> | Justifié  <br/> |**visHorzJustify** <br/> |
| 4  <br/> | Justification forcée  <br/> |**visHorzForce** <br/> |
   
## <a name="remarks"></a>Note

La justification ajoute des espaces entre les mots de toutes les lignes, à l'exception de la dernière ligne du paragraphe, pour aligner les côtés gauche et droit du texte sur les marges.
  
La justification forcée aligne toutes les lignes du paragraphe, y compris la dernière.
  
Pour obtenir une référence à la cellule HAlign par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Para.HorzAlign [ *i* ] où *i* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule HAlign par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionParagraph** <br/> |
| Index de la ligne :  <br/> |**visRowParagraph** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visHorzAlign** <br/> |
   

