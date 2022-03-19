---
title: PageHeight, cellule (section Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm760
ms.localizationpriority: medium
ms.assetid: 0184814c-2d67-6ad4-e336-5694612e518d
description: Contient la hauteur de la page imprimée en unités de dessin.
ms.openlocfilehash: 6a1dbe79071871dc0bcd584d849abce184c6ce55
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63628417"
---
# <a name="pageheight-cell-page-properties-section"></a>PageHeight, cellule (section Page Properties)

Contient la hauteur de la page imprimée en unités de dessin.
  
## <a name="remarks"></a>Remarques

Vous pouvez également définir la hauteur de la page sous l’onglet **Taille de la page** de la boîte de dialogue **Mise en page** (sous l’onglet **Création**, cliquez sur la flèche **Mise en page**) ou en redimensionnant manuellement la page avec la souris. 
  
Pour obtenir une référence à la cellule PageHeight par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de la cellule :**  <br/> |PageHeight  <br/> |
   
Pour obtenir une référence à la cellule PageHeight à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRowPage** <br/> |
|**Index de la cellule :**  <br/> |**visPageHeight** <br/> |
   

