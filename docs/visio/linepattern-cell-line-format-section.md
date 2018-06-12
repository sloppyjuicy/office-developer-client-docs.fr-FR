---
title: LinePattern, cellule (section Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm560
localization_priority: Normal
ms.assetid: a416762b-7294-c99f-d9f1-332c3ed35dff
description: Détermine le motif de trait d'une forme. La valeur entrée dans la cellule LinePattern est un nombre correspondant à un index d'un ensemble de motifs de trait.
ms.openlocfilehash: cccc6028de21299942e62c53aba48622baa95f98
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788954"
---
# <a name="linepattern-cell-line-format-section"></a>LinePattern, cellule (section Line Format)

Détermine le motif de trait d'une forme. La valeur entrée dans la cellule LinePattern est un nombre correspondant à un index d'un ensemble de motifs de trait.
  
|**Valeur**|**Description**|
|:-----|:-----|
|0  <br/> |Aucun motif de trait  <br/> |
|1  <br/> |Uni  <br/> |
|2 - 23  <br/> |Motifs de trait assortis  <br/> |
   
## <a name="remarks"></a>Note

Vous pouvez afficher l’ensemble des motifs de trait dans la boîte de dialogue **trait** (sous l’onglet **accueil** , dans le groupe **forme** , cliquez sur **trait**, pointez sur **tirets**, puis cliquez sur **Autres traits**).
  
Pour choisir un motif de trait personnalisé, utilisez la fonction USE dans cette cellule.
  
Pour obtenir une référence à la cellule LinePattern par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |LinePattern  <br/> |
   
Pour obtenir une référence à la cellule LinePattern par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowLine** <br/> |
|Index de la cellule :  <br/> |**visLinePattern** <br/> |
   

