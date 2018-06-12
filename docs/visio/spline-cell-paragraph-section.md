---
title: SpLine, cellule (section Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm970
localization_priority: Normal
ms.assetid: 84f4e5f1-7c28-9e83-8644-28d117bb10a5
description: Détermine la distance séparant une ligne de texte de la suivante, exprimée en pourcentage, où 100 % représente la hauteur d'une ligne de texte.
ms.openlocfilehash: f2f290564d49a056bc3366707b25a7991f8c4401
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789795"
---
# <a name="spline-cell-paragraph-section"></a>SpLine, cellule (section Paragraph)

Détermine la distance séparant une ligne de texte de la suivante, exprimée en pourcentage, où 100 % représente la hauteur d'une ligne de texte.
  
|**Valeur**|**Description**|
|:-----|:-----|
| \>0  <br/> | Espacement absolu, quelle que soit la taille en points des caractères  <br/> |
| =0  <br/> | Total (espacement = 100 % de la taille des caractères)  <br/> |
| \<0  <br/> | Un pourcentage de la taille des caractères (par exemple, -120 % donne un espacement de 120 %)  <br/> |
   
## <a name="remarks"></a>Note

Pour obtenir une référence à la cellule SpLine par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Paragraphe. SpLine [ *i* ] où *i* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule SpLine par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionParagraph** <br/> |
| Index de la ligne :  <br/> |**visRowParagraph** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visSpaceLine** <br/> |
   

