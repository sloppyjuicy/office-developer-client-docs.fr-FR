---
title: CenterX, cellule (section Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60030
localization_priority: Normal
ms.assetid: 890e2537-66a5-2863-c78d-320b42565ea7
description: Détermine si la page de dessin est centrée horizontalement sur la page d'impression.
ms.openlocfilehash: 13b05ed71248a3f8fada947fca6b203c6ab19c6d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418077"
---
# <a name="centerx-cell-print-properties-section"></a>CenterX, cellule (section Print Properties)

Détermine si la page de dessin est centrée horizontalement sur la page d'impression. 
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | Centre la page de dessin horizontalement sur la page d'impression.  <br/> |
| FALSE  <br/> | Ne centre pas la page de dessin horizontalement sur la page d'impression (valeur par défaut).  <br/> |
   
## <a name="remarks"></a>Remarques

Par défaut, les pages de dessins sont alignées sur le haut et la gauche de la page d'impression. Définir les cellules CenterX et CenterY sur TRUE place la page de dessin au centre de la page d'impression (ou les pages lorsque la mosaïque est nécessaire). 
  
Pour obtenir une référence à la cellule CenterX par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Center  <br/> |
   
Pour obtenir une référence à la cellule CenterX à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowPrintProperties** <br/> |
| Index de la cellule :  <br/> |**visPrintPropertiesCenterX** <br/> |
   

