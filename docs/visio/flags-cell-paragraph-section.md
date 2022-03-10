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
ms.openlocfilehash: 09a3eba44c1e618f0df9eeb078925a05012ed7de
ms.sourcegitcommit: 4164855836af53a068bbbc5b5d126f83ee83e324
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2022
ms.locfileid: "63426936"
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
  
||Valeur |
|:-----|:-----|
|**Nom de cellule :**  <br/> |Para.Flags[ *i*  ] où  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule Flags à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionParagraph** <br/> |
|**Index de la ligne :**  <br/> |**visRowParagraph** +   *i* où *i* = 0, 1, 2... |
|**Index de la cellule :**  <br/> |**visFlags** <br/> |
   

