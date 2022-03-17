---
title: PageShapeSplit, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033777
ms.localizationpriority: medium
ms.assetid: 4d3bdf77-0ad4-86a4-d215-1d5a5fbe33f7
description: Indique si les formes de la page peuvent être fractionnées automatiquement.
ms.openlocfilehash: 35f6f3be0f856940278d24862eda14a436f07b1a
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63522371"
---
# <a name="pageshapesplit-cell-page-layout-section"></a>PageShapeSplit, cellule (section Page Layout)

Indique si les formes de la page peuvent être fractionnées automatiquement.
  
|**Valeur**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
|0  <br/> |Ne pas autoriser le fractionnement automatique des formes. |**visPLOSplitNone** <br/> |
|1  <br/> |Autoriser le fractionnement automatique des formes (valeur par défaut). |**visPLOSplitAllow** <br/> |
   
## <a name="remarks"></a>Remarques

Le fractionnement automatique des formes est activé et désactivé à trois niveaux différents : application, page et forme. Par défaut, le fractionnement est activé aux niveaux application et page. Le paramètre par défaut pour les formes varie en fonction du type de dessin. 
  
Pour activer ou désactiver le fractionnement au niveau de l’application, utilisez le paramètre Activer le  fractionnement de connecteur sous l’onglet Avancé de la boîte de dialogue **Options Visio** (cliquez sur le bouton **Office**, cliquez sur **Options** sous l’onglet **Visio**, puis cliquez sur Options **avancées).** 
  
Pour activer ou désactiver le fractionnement au niveau de la forme, voir les cellules ShapeSplit et ShapeSplittable. 
  
Pour obtenir une référence à la cellule PageShapeSplit par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de cellule :**  <br/> |PageShapeSplit  <br/> |
   
Pour obtenir une référence à la cellule PageShapeSplit à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRowPageLayout** <br/> |
|**Index de la cellule :**  <br/> |**visPLOSplit** <br/> |
   

