---
title: Flags, cellule (section Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033782
localization_priority: Normal
ms.assetid: 898bf89d-d00f-9769-a89d-787ef708eca5
description: Indique si l'orientation du texte est de gauche à droite ou de droite à gauche.
ms.openlocfilehash: af1e79b13d3d8bab2e7271eb79e68cf931871806
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346220"
---
# <a name="flags-cell-paragraph-section"></a>Flags, cellule (section Paragraph)

Indique si l'orientation du texte est de gauche à droite ou de droite à gauche.
  
|**Value**|**Description**|
|:-----|:-----|
|0  <br/> |Orientation du texte de gauche à droite (valeur par défaut).  <br/> |
|0,1  <br/> |Orientation du texte de droite à gauche.  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur de cette cellule correspond au paramètre **direction** de l'onglet **paragraphe** de la boîte de dialogue **texte** (sous l'onglet **Accueil** , cliquez sur la flèche **police** ), qui s'affiche uniquement si une langue qui utilise du texte de scripts complexes a été ajouté dans la boîte de dialogue **Préférences de langue de Microsoft Office** . (Cliquez **sur Démarrer**, **sur tous les programmes**, sur **Microsoft Office**, sur **outils Microsoft Office**, puis sur **Préférences de langue de Microsoft Office**.) 
  
Pour obtenir une référence à la cellule Flags par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |Para. Flags [ *i* ] où *i* = <1>, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule Flags à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionParagraph** <br/> |
|Index de la ligne :  <br/> |**visRowParagraph** +  *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visFlags** <br/> |
   

