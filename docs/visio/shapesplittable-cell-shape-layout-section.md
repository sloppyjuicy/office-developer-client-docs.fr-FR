---
title: ShapeSplittable, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60081
localization_priority: Normal
ms.assetid: 6330304a-71f3-62b4-1b27-14495e3f12c3
description: Indique si cette forme 1D peut être fractionnée.
ms.openlocfilehash: e2db881465a19b34d5788f1621f15c4d7d15c293
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789681"
---
# <a name="shapesplittable-cell-shape-layout-section"></a>ShapeSplittable, cellule (section Shape Layout)

Indique si cette forme 1D peut être fractionnée. 
  
|**Valeur**|**Description**|**Constante d’Automation**|
|:-----|:-----|:-----|
| 0  <br/> | Ne pas autoriser cette forme à être fractionnée.  <br/> |**visSLOSplittableNone** <br/> |
| 1  <br/> | Autoriser cette forme à être fractionnée.  <br/> |**visSLOSplittableAllow** <br/> |
   
## <a name="remarks"></a>Note

Le comportement par défaut des connecteurs et autres formes 1D varie en fonction du type de dessin. 
  
Le fractionnement automatique des formes est activé et désactivé à trois niveaux différents : application, page et forme. Par défaut, le fractionnement est activé aux niveaux de l’application et de la page. 
  
Pour activer ou désactiver le fractionnement au niveau de l’application, utilisez le paramètre **Autoriser le fractionnement** sur l’onglet **Avancé** de la boîte de dialogue **Options Visio** (cliquez sur l’onglet **fichier** , cliquez sur **Options**, puis cliquez sur ** Avancés** ). 
  
Pour activer ou désactiver le fractionnement sur une page, reportez-vous à la cellule [PageShapeSplit](pageshapesplit-cell-page-layout-section.md) . 
  
Pour qu’une forme peut fractionner les formes fractionnables 1-D, reportez-vous à la cellule [ShapeSplit](shapesplit-cell-shape-layout-section.md) . 
  
Pour obtenir une référence à la cellule ShapleSplittable par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | ShapeSplittable  <br/> |
   
Pour obtenir une référence à la cellule ShapeSplittable par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowShapeLayout** <br/> |
| Index de la cellule :  <br/> |**visSLOSplittable** <br/> |
   

