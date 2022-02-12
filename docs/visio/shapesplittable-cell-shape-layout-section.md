---
title: ShapeSplittable, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60081
ms.localizationpriority: medium
ms.assetid: 6330304a-71f3-62b4-1b27-14495e3f12c3
description: Indique si cette forme 1D peut être fractionnée.
ms.openlocfilehash: d476c6121959d0e7db411697e85b1a6d576643c8
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62784572"
---
# <a name="shapesplittable-cell-shape-layout-section"></a>ShapeSplittable, cellule (section Shape Layout)

Indique si cette forme 1D peut être fractionnée. 
  
|**Valeur**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
| 0  <br/> | Ne pas autoriser cette forme à être fractionnée. |**visSLOSplittableNone** <br/> |
| 1  <br/> | Autoriser cette forme à être fractionnée. |**visSLOSplittableAllow** <br/> |
   
## <a name="remarks"></a>Remarques

Le comportement par défaut des connecteurs et autres formes 1D varie en fonction du type de dessin. 
  
Le fractionnement automatique des formes est activé et désactivé à trois niveaux différents : application, page et forme. Par défaut, le fractionnement est activé aux niveaux de l’application et de la page. 
  
Pour activer ou désactiver le fractionnement au niveau de l’application, utilisez le paramètre Activer le  fractionnement de connecteur sous l’onglet Avancé de la boîte de dialogue  **Options Visio** (cliquez sur l’onglet Fichier, sur **Options**, puis sur Options **avancées).** 
  
Pour activer ou désactiver le fractionnement sur une page, consultez la rubrique de la cellule [PageShapeSplit](pageshapesplit-cell-page-layout-section.md). 
  
Pour savoir comment une forme peut fractionner les formes 1D fractionnables, consultez la rubrique de la cellule [ShapeSplit](shapesplit-cell-shape-layout-section.md). 
  
Pour obtenir une référence à la cellule ShapeSplittable par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | ShapeSplittable  <br/> |
   
Pour obtenir une référence à la cellule ShapeSplittable à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowShapeLayout** <br/> |
| Index de la cellule :  <br/> |**visSLOSplittable** <br/> |
   

