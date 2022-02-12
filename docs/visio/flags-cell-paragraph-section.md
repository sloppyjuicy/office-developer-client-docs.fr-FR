---
title: Flags, cellule (section Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033782
ms.localizationpriority: medium
ms.assetid: 898bf89d-d00f-9769-a89d-787ef708eca5
description: Indique si l'orientation du texte est de gauche à droite ou de droite à gauche.
ms.openlocfilehash: 2d87143b5bbcb1bcadcbc1833a54a9e4bfc37732
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62777214"
---
# <a name="flags-cell-paragraph-section"></a>Flags, cellule (section Paragraph)

Indique si l'orientation du texte est de gauche à droite ou de droite à gauche.
  
|**Valeur**|**Description**|
|:-----|:-----|
|0  <br/> |Orientation du texte de gauche à droite (valeur par défaut). |
|1  <br/> |Orientation du texte de droite à gauche. |
   
## <a name="remarks"></a>Remarques

La valeur de cette cellule correspond au paramètre **Direction** sous l’onglet  Paragraphe de la boîte  de dialogue Texte (sous l’onglet Accueil, cliquez  sur la flèche Police), qui apparaît uniquement si une langue qui utilise du texte de scripts complexes a été ajoutée dans la boîte de dialogue Préférences de langue **Microsoft Office**. (Cliquez **sur** Démarrer, sur Tous les **programmes, sur** **Microsoft Office**, sur Microsoft Office **Outils**, puis sur Microsoft Office **langue.**) 
  
Pour obtenir une référence à la cellule Flags par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |Para.Flags[ *i*  ] où  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule Flags à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionParagraph** <br/> |
|Index de la ligne :  <br/> |**visRowParagraph** +   *i* où *i* = 0, 1, 2... |
|Index de la cellule :  <br/> |**visFlags** <br/> |
   

