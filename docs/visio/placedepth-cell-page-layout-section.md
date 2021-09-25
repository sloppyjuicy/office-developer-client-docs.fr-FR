---
title: PlaceDepth, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1230
ms.localizationpriority: medium
ms.assetid: 02c139db-fe67-f550-1d07-8c8a9a4fb427
description: Détermine la méthode utilisée pour analyser le dessin avant la création de la mise en page et définit le type de mise en page.
ms.openlocfilehash: 10c116de99cce8fce65b6949341174aa6a3cf6b4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559779"
---
# <a name="placedepth-cell-page-layout-section"></a>PlaceDepth, cellule (section Page Layout)

Détermine la méthode utilisée pour analyser le dessin avant la création de la mise en page et définit le type de mise en page.
  
|**Valeur**|**Profondeur de placement pour les mises en page verticales et horizontales**|**Constante d'automation**|
|:-----|:-----|:-----|
| 0  <br/> | Valeur par défaut de la page  <br/> |**visPLOPlaceDepthDefault** <br/> |
| 1  <br/> | Moyenne  <br/> |**visPLOPlaceDepthMedium** <br/> |
| 2  <br/> | Deep  <br/> |**visPLOPlaceDepthDeep** <br/> |
| 3  <br/> | Superficiel  <br/> |**visPLOPlaceDepthShallow** <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule PlaceDepth par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | PlaceDepth  <br/> |
   
Pour obtenir une référence à la cellule PlaceDepth à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowPageLayout** <br/> |
| Index de la cellule :  <br/> |**visPLOPlaceDepth** <br/> |
   

