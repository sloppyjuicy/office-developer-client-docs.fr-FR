---
title: LineWeight, cellule (section Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm585
localization_priority: Normal
ms.assetid: 16b0e293-eeef-34b4-aeb0-4472815dd543
description: Détermine l’épaisseur d’un trait. Pour définir l’épaisseur, entrez un nombre accompagné d’une unité de mesure valide.
ms.openlocfilehash: a5207607d90ef6a79dcb3acc191521b73e2cdf54
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788962"
---
# <a name="lineweight-cell-line-format-section"></a>LineWeight, cellule (section Line Format)

Détermine l’épaisseur d’un trait. Pour définir l’épaisseur, entrez un nombre accompagné d’une unité de mesure valide.
  
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de LineWeight dans la boîte de dialogue **trait** (sous l’onglet **accueil** , dans le groupe **forme** , cliquez sur **trait**, pointez sur **poids**, puis cliquez sur **Autres traits**).
  
Si l’unité de mesure n’est pas entrée, l’unité de mesure pour le texte spécifié dans la boîte de dialogue **Options Visio** est utilisée (cliquez sur l’onglet **fichier** , puis cliquez sur **Options**). Épaisseur de trait est indépendante de l’échelle du dessin. Si le dessin est mis à l’échelle, l’épaisseur de trait reste identique. 
  
Pour obtenir une référence à la cellule LineWeight par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Épaisseur de trait  <br/> |
   
Pour obtenir une référence à la cellule LineWeight par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowLine** <br/> |
| Index de la cellule :  <br/> |**visLineWeight** <br/> |
   

