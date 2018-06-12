---
title: ShapeSplit, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60080
localization_priority: Normal
ms.assetid: 96b8c503-67b3-8623-d99b-0dad7b15c224
description: Indique si cette forme peut fractionner les formes fractionnables.
ms.openlocfilehash: b782977bd5b7e828223675eb16f4e7e48f4ca55d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789674"
---
# <a name="shapesplit-cell-shape-layout-section"></a>ShapeSplit, cellule (section Shape Layout)

Indique si cette forme peut fractionner les formes fractionnables.
  
|**Valeur**|**Description**|**Constante d’Automation**|
|:-----|:-----|:-----|
| 0  <br/> | Ne pas autoriser cette forme à en fractionner d’autres.  <br/> |**visSLOSplitNone** <br/> |
| 1  <br/> | Autoriser cette forme à en fractionner d’autres.  <br/> |**visSLOSplitAllow** <br/> |
   
## <a name="remarks"></a>Note

Une forme qui peut en fractionner d’autres doit être une forme 2D ou une forme 1D positionnable. 
  
Le fractionnement automatique des formes est activé et désactivé à trois niveaux différents : application, page et forme. Par défaut, le fractionnement est activé aux niveaux application et page ; pour les formes, il varie en fonction du type de dessin. 
  
Pour activer ou désactiver le fractionnement au niveau de l’application, utilisez le paramètre **Autoriser le fractionnement** sur l’onglet **Avancé** de la boîte de dialogue **Options Visio** (cliquez sur l’onglet **fichier** , cliquez sur **Options**, puis cliquez sur ** Avancés**). 
  
Pour activer ou désactiver le fractionnement sur une page, reportez-vous à la cellule PageShapeSplit. 
  
Pour rendre une forme 1D fractionnable, reportez-vous à la cellule ShapeSplittable.
  
Pour obtenir une référence à la cellule ShapeSplit par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | ShapeSplit  <br/> |
   
Pour obtenir une référence à la cellule ShapeSplit par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowShapeLayout** <br/> |
| Index de la cellule :  <br/> |**visSLOSplit** <br/> |
   

