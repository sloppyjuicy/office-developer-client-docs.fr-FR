---
title: CenterY, cellule (section Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033792
localization_priority: Normal
ms.assetid: 7ce0bf66-dc8b-9646-7b04-50c969ecd67a
description: Détermine si la page de dessin est centrée verticalement sur la page d'impression.
ms.openlocfilehash: 2fde1d6301d7b9de4540cd12f21e5af01d7a6239
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788266"
---
# <a name="centery-cell-print-properties-section"></a>CenterY, cellule (section Print Properties)

Détermine si la page de dessin est centrée verticalement sur la page d'impression. 
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | Centre la page de dessin verticalement sur la page d'impression.  <br/> |
| FALSE  <br/> | Ne centre pas la page de dessin verticalement sur la page d'impression (valeur par défaut).  <br/> |
   
## <a name="remarks"></a>Note

Par défaut, les pages de dessins sont alignées sur le haut et la gauche de la page d'impression. Définir les cellules CenterX et CenterY sur TRUE place la page de dessin au centre de la page d'impression (ou les pages lorsque la mosaïque est nécessaire). 
  
Pour obtenir une référence à la cellule CenterY par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | CenterY  <br/> |
   
Pour obtenir une référence à la cellule CenterY par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowPrintProperties** <br/> |
| Index de la cellule :  <br/> |**visPrintPropertiesCenterY** <br/> |
   

