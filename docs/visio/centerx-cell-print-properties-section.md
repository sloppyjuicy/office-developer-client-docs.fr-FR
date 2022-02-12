---
title: CenterX, cellule (section Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60030
ms.localizationpriority: medium
ms.assetid: 890e2537-66a5-2863-c78d-320b42565ea7
description: Détermine si la page de dessin est centrée horizontalement sur la page d'impression.
ms.openlocfilehash: 4adfe7c43e7e8ef2ec52ce391422518191ad2e67
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62774453"
---
# <a name="centerx-cell-print-properties-section"></a>CenterX, cellule (section Print Properties)

Détermine si la page de dessin est centrée horizontalement sur la page d'impression. 
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | Centre la page de dessin horizontalement sur la page d'impression. |
| FALSE  <br/> | Ne centre pas la page de dessin horizontalement sur la page d'impression (valeur par défaut). |
   
## <a name="remarks"></a>Remarques

Par défaut, les pages de dessins sont alignées sur le haut et la gauche de la page d'impression. Définir les cellules CenterX et CenterY sur TRUE place la page de dessin au centre de la page d'impression (ou les pages lorsque la mosaïque est nécessaire). 
  
Pour obtenir une référence à la cellule CenterX par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | CenterX  <br/> |
   
Pour obtenir une référence à la cellule CenterX à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowPrintProperties** <br/> |
| Index de la cellule :  <br/> |**visPrintPropertiesCenterX** <br/> |
   

