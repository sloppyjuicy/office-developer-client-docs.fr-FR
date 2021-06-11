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
description: La fenêtre Suivi des formules est conçue pour fournir aux développeurs de formes des informations à propos d’interdépendances entre des cellules — à la fois des cellules dépendantes (qui dépendent d’une cellule en particulier) et des cellules précédentes (dont dépend une cellule en particulier).
ms.openlocfilehash: f5f9d6a7ba3ab7049715d31342cfe7aa68ea053f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345315"
---
# <a name="about-the-formula-tracing-window"></a>À propos de la fenêtre Suivi des formules

La fenêtre **Suivi des formules** est conçue pour fournir aux développeurs de formes des informations à propos d’interdépendances entre des cellules — à la fois des cellules dépendantes (qui dépendent d’une cellule en particulier) et des cellules précédentes (dont dépend une cellule en particulier). 
  
Les cellules d’une feuille ShapeSheet Microsoft Visio contiennent des valeurs et des formules. Les formules peuvent, à leur tour, avoir des références à d’autres cellules, ce qui vous donne la puissance de calculer une valeur dans une cellule en fonction de la valeur d’une autre cellule. Toutefois, en créant ou en maintenant des formes complexes, il peut s’avérer difficile d’identifier toutes ces interdépendances car une formule peut faire référence à n’importe quelle cellule du dessin, qu’il s’agisse d’une cellule de la même feuille ShapeSheet ou d’une cellule appartenant à un autre objet du dessin comme une page, un style, une forme de base ou une autre forme. 
  
La **fenêtre Suivi des** formules fournit des informations pour vous aider à comprendre les implications des modifications apportées aux cellules. 
  
## <a name="displaying-the-formula-tracing-window"></a>Affichage de la fenêtre Suivi des formules

Pour afficher  la fenêtre Suivi des formules, avec la fenêtre Feuille ShapeSheet active,  sous Outils **Feuille ShapeSheet** sous l’onglet ** Création **, dans le groupe Suivi des formules, cliquez sur **Afficher la fenêtre.** La  fenêtre Suivi des formules apparaît ancrée dans la fenêtre Feuille ShapeSheet par défaut, mais il s’agit d’une fenêtre ancrée qui peut être ancrée, flottante ou fusionnée avec d’autres fenêtres ShapeSheet ancrées disponibles, par exemple la fenêtre Explorateur de **styles.** 
  
## <a name="tracing-dependent-cells"></a>Cellules Tracing dependent

Pour une liste des cellules dépendantes d’une cellule en particulier, sélectionnez cette cellule dans la fenêtre ShapeSheet. Dans cet exemple, la cellule Width est sélectionnée. 
  
![La cellule Width est sélectionnée](media/ShapeSheetDependents_UI_01_ZA01039814.gif)
  
Pour afficher ses cellules dépendantes, dans le groupe **Suivi** des **formules, cliquez sur Dépendants du suivi.**
  
Une liste reprenant toutes les cellules dépendantes de la cellule Width apparaît dans la fenêtre **Suivi des formules**. Vous pouvez accéder à n’importe quelle cellule de la liste en double-cliquant sur son entrée dans la fenêtre **Suivi des formules**. 
  
![Toutes les cellules ayant une dépendance sur la cellule Width apparaissent dans la fenêtre Suivi des formules](media/ShapeSheetDependents_UI_02_ZA01039815.gif)
  
## <a name="tracing-precendent-cells"></a>Cellules pré-cendentes de suivi

Pour une liste des cellules dont une cellule en particulier est dépendante, sélectionnez d’abord la cellule dans la fenêtre ShapeSheet. Dans cet exemple, Ia cellule Geometry1.X2 est sélectionnée. 
  
![La cellule Geometry1.X2 est sélectionnée](media/ShapeSheetPrecedents_UI_01_ZA01039817.gif)
  
Pour afficher ses cellules précédentes, dans le groupe **Suivi** des formules, cliquez **sur Suivi des antécédents.**
  
La liste de toutes les cellules dont dépend la cellule Geometry1.X2 apparaît dans la fenêtre Suivi **des** formules. Vous pouvez accéder à n’importe quelle cellule de la liste en double-cliquant sur son entrée dans la fenêtre **Suivi des formules**. 
  
![Toutes les cellules dont dépend la cellule Geometry1.X2 apparaissent dans la fenêtre Suivi des formules](media/ShapeSheetPrecedents_UI_02_ZA01039818.gif)
  

