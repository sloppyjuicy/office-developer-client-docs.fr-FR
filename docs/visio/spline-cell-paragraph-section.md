---
title: SpLine, cellule (section Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm970
ms.localizationpriority: medium
ms.assetid: 84f4e5f1-7c28-9e83-8644-28d117bb10a5
description: Détermine la distance séparant une ligne de texte de la suivante, exprimée en pourcentage, où 100 % représente la hauteur d'une ligne de texte.
ms.openlocfilehash: 38a565eafcdd64da9fe4dfb041e76c584e392322
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59553780"
---
# <a name="spline-cell-paragraph-section"></a>SpLine, cellule (section Paragraph)

Détermine la distance séparant une ligne de texte de la suivante, exprimée en pourcentage, où 100 % représente la hauteur d'une ligne de texte.
  
|**Valeur**|**Description**|
|:-----|:-----|
| \>0  <br/> | Espacement absolu, quelle que soit la taille en points des caractères  <br/> |
| =0  <br/> | Total (espacement = 100 % de la taille des caractères)  <br/> |
| \<0  <br/> | Un pourcentage de la taille des caractères (par exemple, -120 % donne un espacement de 120 %)  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule SpLine par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Para. SpLine [  *i*  ] où  *i*  = <1>, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule SpLine dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionParagraph** <br/> |
| Index de la ligne :  <br/> |**visRowParagraph**  +   *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visSpaceLine** <br/> |
   

