---
title: ShapeSplit, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60080
ms.localizationpriority: medium
ms.assetid: 96b8c503-67b3-8623-d99b-0dad7b15c224
description: Indique si cette forme peut fractionner les formes fractionnables.
ms.openlocfilehash: da89333e8a190d2ad573b1d088480c5e0df6efd8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549608"
---
# <a name="shapesplit-cell-shape-layout-section"></a>ShapeSplit, cellule (section Shape Layout)

Indique si cette forme peut fractionner les formes fractionnables.
  
|**Valeur**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
| 0  <br/> | Ne pas autoriser cette forme à en fractionner d’autres.  <br/> |**visSLOSplitNone** <br/> |
| 1  <br/> | Autoriser cette forme à en fractionner d’autres.  <br/> |**visSLOSplitAllow** <br/> |
   
## <a name="remarks"></a>Remarques

Une forme qui peut en fractionner d’autres doit être une forme 2D ou une forme 1D positionnable. 
  
Le fractionnement automatique des formes est activé et désactivé à trois niveaux différents : application, page et forme. Par défaut, le fractionnement est activé aux niveaux application et page ; pour les formes, il varie en fonction du type de dessin. 
  
Pour activer ou désactiver le fractionnement  au niveau de  l’application, utilisez le paramètre Activer  le fractionnement de connecteur sous l’onglet Avancé de la boîte de dialogue **Options Visio** (cliquez sur l’onglet Fichier, cliquez sur **Options,** puis sur **Options** avancées). 
  
Pour activer ou désactiver le fractionnement sur une page, reportez-vous à la cellule PageShapeSplit. 
  
Pour rendre une forme 1D fractionnable, reportez-vous à la cellule ShapeSplittable.
  
Pour obtenir une référence à la cellule ShapeSplit par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU,** utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | ShapeSplit  <br/> |
   
Pour obtenir une référence à la cellule ShapeSplit à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowShapeLayout** <br/> |
| Index de la cellule :  <br/> |**visSLOSplit** <br/> |
   

