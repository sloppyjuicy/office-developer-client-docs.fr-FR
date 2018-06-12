---
title: PageShapeSplit, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033777
localization_priority: Normal
ms.assetid: 4d3bdf77-0ad4-86a4-d215-1d5a5fbe33f7
description: Indique si les formes de la page peuvent être fractionnées automatiquement.
ms.openlocfilehash: 7f1df0158cde6853c5518597c853cb56151eefbc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789222"
---
# <a name="pageshapesplit-cell-page-layout-section"></a>PageShapeSplit, cellule (section Page Layout)

Indique si les formes de la page peuvent être fractionnées automatiquement.
  
|**Valeur**|**Description**|**Constante d’Automation**|
|:-----|:-----|:-----|
|0  <br/> |Ne pas autoriser le fractionnement automatique des formes.  <br/> |**visPLOSplitNone** <br/> |
|1  <br/> |Autoriser le fractionnement automatique des formes (valeur par défaut).  <br/> |**visPLOSplitAllow** <br/> |
   
## <a name="remarks"></a>Note

Le fractionnement automatique des formes est activé et désactivé à trois niveaux différents : application, page et forme. Par défaut, le fractionnement est activé aux niveaux application et page. Le paramètre par défaut pour les formes varie en fonction du type de dessin. 
  
Pour activer ou désactiver le fractionnement au niveau de l’application, utilisez le paramètre **Autoriser le fractionnement** sur l’onglet **Avancé** de la boîte de dialogue **Options Visio** (cliquez sur le bouton **Office** , cliquez sur **Options** dans **Visio** onglet, puis cliquez sur **Options avancées** ). 
  
Pour activer ou désactiver le fractionnement au niveau forme, reportez-vous aux cellules ShapeSplit et ShapeSplittable. 
  
Pour obtenir une référence à la cellule PageShapeSplit par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |PageShapeSplit  <br/> |
   
Pour obtenir une référence à la cellule PageShapeSplit par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowPageLayout** <br/> |
|Index de la cellule :  <br/> |**visPLOSplit** <br/> |
   

