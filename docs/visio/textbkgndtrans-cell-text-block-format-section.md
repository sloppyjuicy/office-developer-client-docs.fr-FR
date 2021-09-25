---
title: TextBkgndTrans, cellule (section Text Block Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253240
ms.localizationpriority: medium
ms.assetid: b2f9d317-cc42-bec5-66f9-f988bcbdcc24
description: Détermine le niveau de transparence de la couleur d'arrière-plan du bloc de texte de la forme.
ms.openlocfilehash: c376f56ffca919b9f07798b3f3da419463b805f4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597890"
---
# <a name="textbkgndtrans-cell-text-block-format-section"></a>TextBkgndTrans, cellule (section Text Block Format)

Détermine le niveau de transparence de la couleur d'arrière-plan du bloc de texte de la forme.
  
|**Valeur**|**Description**|
|:-----|:-----|
|0 - 100  <br/> |Représente le pourcentage de transparence. La valeur par défaut est 0 % (entièrement opaque).  <br/> |
   
## <a name="remarks"></a>Remarques

Les valeurs sont arrondies au pourcentage le plus proche. Une valeur de 100 % correspond à une transparence totale. Même si une forme dont l’arrière-plan de texte est entièrement transparent apparaît identique sur la page de dessin à une forme dépourvue d’arrière-plan de texte, elle interagit avec les autres objets de la page de la même façon que si elle avait une transparence de 0 %.
  
Vous pouvez également définir cette valeur à l’aide du curseur sous l’onglet **Police** de la boîte de dialogue **Texte** (sous l’onglet **Accueil**, cliquez sur la flèche **Police**). 
  
Pour obtenir une référence à la cellule TextBkgndTrans par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |TextBkgndTrans  <br/> |
   
Pour obtenir une référence à la cellule TextBkgndTrans par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowText** <br/> |
|Index de la cellule :  <br/> |**visTxtBlkBkgndTrans** <br/> |
   

