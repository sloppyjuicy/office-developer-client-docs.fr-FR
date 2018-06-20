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
ms.openlocfilehash: b471d08556bedf68ce75595b9c211758297e8352
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788633"
---
# <a name="flags-cell-paragraph-section"></a>Flags, cellule (section Paragraph)

Indique si l'orientation du texte est de gauche à droite ou de droite à gauche.
  
|**Valeur**|**Description**|
|:-----|:-----|
|0  <br/> |Orientation du texte de gauche à droite (valeur par défaut).  <br/> |
|1  <br/> |Orientation du texte de droite à gauche.  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur de cette cellule correspond au paramètre **orientation** de l’onglet **paragraphe** dans la boîte de dialogue **texte** (sous l’onglet **accueil** , cliquez sur la flèche **police** ), qui s’affiche uniquement si le texte de scripts une langue qui utilise un type complexe a été ajouté dans la boîte de dialogue **Préférences linguistiques de Microsoft Office** . (Cliquez sur **Démarrer**, sur **Tous les programmes**, sur **Microsoft Office**, sur **Outils Microsoft Office**, puis cliquez sur **Préférences linguistiques de Microsoft Office**.) 
  
Pour obtenir une référence à la cellule Flags par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |Para.Flags [ *i* ] où *i* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule Flags par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionParagraph** <br/> |
|Index de la ligne :  <br/> |**visRowParagraph** +  *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visFlags** <br/> |
   

