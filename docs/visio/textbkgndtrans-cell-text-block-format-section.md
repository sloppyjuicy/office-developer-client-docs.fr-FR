---
title: TextBkgndTrans, cellule (section Text Block Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253240
localization_priority: Normal
ms.assetid: b2f9d317-cc42-bec5-66f9-f988bcbdcc24
description: Détermine le niveau de transparence de la couleur d'arrière-plan du bloc de texte de la forme.
ms.openlocfilehash: d9fee430cb2ccd19e8d6069e7561a8fef409a62e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789874"
---
# <a name="textbkgndtrans-cell-text-block-format-section"></a>TextBkgndTrans, cellule (section Text Block Format)

Détermine le niveau de transparence de la couleur d'arrière-plan du bloc de texte de la forme.
  
|**Valeur**|**Description**|
|:-----|:-----|
|0 - 100  <br/> |Représente le pourcentage de transparence. La valeur par défaut est 0 % (entièrement opaque).  <br/> |
   
## <a name="remarks"></a>Note

Les valeurs sont arrondies au pourcentage le plus proche. Une valeur de 100 % correspond à une transparence totale. Même si une forme dont l’arrière-plan de texte est entièrement transparent apparaît identique sur la page de dessin à une forme dépourvue d’arrière-plan de texte, elle interagit avec les autres objets de la page de la même façon que si elle avait une transparence de 0 %.
  
Vous pouvez également définir cette valeur à l’aide du curseur sous l’onglet **police** de la boîte de dialogue **texte** (sous l’onglet **accueil** , cliquez sur la flèche **police** ). 
  
Pour obtenir une référence à la cellule TextBkgndTrans par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |TextBkgndTrans  <br/> |
   
Pour obtenir une référence à la cellule TextBkgndTrans par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowText** <br/> |
|Index de la cellule :  <br/> |**visTxtBlkBkgndTrans** <br/> |
   

