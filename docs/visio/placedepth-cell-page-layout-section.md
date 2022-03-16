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
ms.openlocfilehash: 3366afac0b9ad64dbdf8716a5746d16a8d15a826
ms.sourcegitcommit: b2c5a02b2d0abd2da2542089fc3f83ff07e121e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2022
ms.locfileid: "63507693"
---
# <a name="placedepth-cell-page-layout-section"></a>PlaceDepth, cellule (section Page Layout)

Détermine la méthode utilisée pour analyser le dessin avant la création de la mise en page et définit le type de mise en page.
  
|**Valeur**|**Profondeur de placement pour les mises en page verticales et horizontales**|**Constante d'automation**|
|:-----|:-----|:-----|
| 0  <br/> | Valeur par défaut de la page  <br/> |**visPLOPlaceDepthDefault** <br/> |
| 1  <br/> | Moyen  <br/> |**visPLOPlaceDepthMedium** <br/> |
| 2  <br/> | Deep  <br/> |**visPLOPlaceDepthDeep** <br/> |
| 3  <br/> | Superficiel  <br/> |**visPLOPlaceDepthShallow** <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule PlaceDepth par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de la cellule :**  <br/> | PlaceDepth  <br/> |
   
Pour obtenir une référence à la cellule PlaceDepth à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowPageLayout** <br/> |
| **Index de la cellule :**  <br/> |**visPLOPlaceDepth** <br/> |
   

