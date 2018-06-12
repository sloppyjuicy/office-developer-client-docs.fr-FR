---
title: PlaceDepth, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1230
localization_priority: Normal
ms.assetid: 02c139db-fe67-f550-1d07-8c8a9a4fb427
description: Détermine la méthode utilisée pour analyser le dessin avant la création de la mise en page et définit le type de mise en page.
ms.openlocfilehash: ab2c83a94c3dd03c1fdbf0c3ee187076406b2e84
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789231"
---
# <a name="placedepth-cell-page-layout-section"></a>PlaceDepth, cellule (section Page Layout)

Détermine la méthode utilisée pour analyser le dessin avant la création de la mise en page et définit le type de mise en page.
  
|**Valeur**|**Profondeur de placement pour les mises en page verticales et horizontales**|**Constante d’Automation**|
|:-----|:-----|:-----|
| 0  <br/> | Valeur par défaut de la page  <br/> |**visPLOPlaceDepthDefault** <br/> |
| 1  <br/> | Moyen  <br/> |**visPLOPlaceDepthMedium** <br/> |
| 2  <br/> | Profond  <br/> |**visPLOPlaceDepthDeep** <br/> |
| 3  <br/> | Peu profond  <br/> |**visPLOPlaceDepthShallow** <br/> |
   
## <a name="remarks"></a>Note

Pour obtenir une référence à la cellule PlaceDepth par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | PlaceDepth  <br/> |
   
Pour obtenir une référence à la cellule PlaceDepth par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowPageLayout** <br/> |
| Index de la cellule :  <br/> |**visPLOPlaceDepth** <br/> |
   

