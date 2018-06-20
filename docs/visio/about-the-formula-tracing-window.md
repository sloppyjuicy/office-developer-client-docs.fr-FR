---
title: À propos de la fenêtre Suivi des formules
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm60118
localization_priority: Normal
ms.assetid: 0cdacd4e-74dc-32c3-2eb2-219bf7fcb532
description: La fenêtre suivi des formules est conçue pour fournir aux développeurs de formes avec des informations sur les interdépendances entre des cellules — à la fois des cellules dépendantes (qui ont une dépendance sur une cellule donnée) et des cellules précédentes (qui dépend d’une cellule donnée).
ms.openlocfilehash: 316ac219f548b2459ea2d0ad8cece0f693957fcf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787984"
---
# <a name="about-the-formula-tracing-window"></a>À propos de la fenêtre Suivi des formules

La fenêtre **Suivi des formules** est conçue pour fournir aux développeurs de formes avec des informations sur les interdépendances entre des cellules — à la fois des cellules dépendantes (qui ont une dépendance sur une cellule donnée) et des cellules précédentes (qui dépend d’une cellule donnée). 
  
Les cellules dans un Microsoft Visio ShapeSheet contiennent des formules et les valeurs. Formules peuvent, à son tour, avoir des références à d’autres cellules, la puissance pour calculer une valeur dans une cellule en fonction de la valeur d’une autre cellule. Lors de la création ou la gestion des formes complexes, toutefois, il peut être difficile à identifier toutes ces interdépendances car une formule peut faire référence à n’importe quelle cellule dans le dessin, qu’il s’agisse d’une cellule dans la même feuille ShapeSheet ou une cellule appartenant à un autre objet dans le dessin, par exemple, une page, style, master ou une autre forme. 
  
La fenêtre **Suivi des formules** fournit des informations pour vous aider à comprendre les implications des changements opérés sur les cellules. 
  
## <a name="displaying-the-formula-tracing-window"></a>Afficher la fenêtre suivi des formules

Pour afficher la fenêtre **Suivi des formules** , avec la fenêtre ShapeSheet active, sous **Outils feuille ShapeSheet** dans le ** conception ** onglet, dans le groupe **Suivi des formules** , cliquez sur **Afficher la fenêtre**. La fenêtre **Suivi des formules** apparaît fixe par défaut dans la fenêtre feuille ShapeSheet, mais est une fenêtre ancrée qui peut être fixe, flottante ou fusionnée avec d’autres fenêtres ShapeSheet ancrées disponibles, par exemple, la fenêtre **Explorateur de styles** . 
  
## <a name="tracing-dependent-cells"></a>Cellules Tracing dependent

Pour une liste des cellules dépendantes d’une cellule en particulier, sélectionnez cette cellule dans la fenêtre ShapeSheet. Dans cet exemple, la cellule Width est sélectionnée. 
  
![](media/ShapeSheetDependents_UI_01_ZA01039814.gif)
  
Pour afficher ses cellules dépendantes, dans le groupe **Suivi des formules**, cliquez sur **Repérer les dépendants**.
  
Une liste de toutes les cellules avec une dépendance sur la cellule Width apparaît dans la fenêtre **Suivi des formules** . Vous pouvez accéder à n’importe quelle cellule dans la liste en double-cliquant sur son entrée dans la fenêtre **Suivi des formules** . 
  
![](media/ShapeSheetDependents_UI_02_ZA01039815.gif)
  
## <a name="tracing-precendent-cells"></a>Suivi des cellules precendent

Pour une liste des cellules dont une cellule en particulier est dépendante, sélectionnez d’abord la cellule dans la fenêtre ShapeSheet. Dans cet exemple, Ia cellule Geometry1.X2 est sélectionnée. 
  
![](media/ShapeSheetPrecedents_UI_01_ZA01039817.gif)
  
Pour afficher ses cellules dépendantes, dans le groupe **Suivi des formules**, cliquez sur **Repérer les antécédents**.
  
Une liste de toutes les cellules dont dépend la cellule Geometry1.X2 apparaît dans la fenêtre **Suivi des formules** . Vous pouvez accéder à n’importe quelle cellule dans la liste en double-cliquant sur son entrée dans la fenêtre **Suivi des formules** . 
  
![](media/ShapeSheetPrecedents_UI_02_ZA01039818.gif)
  

