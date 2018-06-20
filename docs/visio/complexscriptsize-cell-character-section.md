---
title: ComplexScriptSize, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033768
localization_priority: Normal
ms.assetid: f58687d7-2ba4-ff77-0bcc-3106867d89de
description: Taille de la police utilisée pour mettre en forme du texte composé de caractères de script complexe.
ms.openlocfilehash: 4867ab57fa59b3a5e76598108fbb92b9bbab7913
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788308"
---
# <a name="complexscriptsize-cell-character-section"></a>ComplexScriptSize, cellule (section Character)

Taille de la police utilisée pour mettre en forme du texte composé de caractères de script complexe. 
  
## <a name="remarks"></a>Remarques

Tailles de police des scripts complexes sont répertoriés sous l’onglet **police** de la boîte de dialogue **texte** (cliquez sur la flèche dans la **police** de groupe sous l’onglet **accueil** ). Cette liste apparaît uniquement si vous avez ajouté une langue qui contienne des caractères asiatiques ou à script complexe, dans la boîte de dialogue **Préférences linguistiques de Microsoft Office** . (Cliquez sur **Démarrer**, sur **Tous les programmes**, sur **Microsoft Office**, sur **Outils Microsoft Office**, puis cliquez sur **Préférences linguistiques de Microsoft Office**.
  
Vous pouvez entrer cette valeur comme taille de point explicite ou comme pourcentage. Si vous indiquez un pourcentage, la valeur est basée sur celle de la cellule Size. Une valeur par défaut de 0 (zéro) signifie 100 %. 
  
Pour obtenir une référence à la cellule ComplexScriptSize par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |Char.ComplexScriptSize [ *i* ] où *i* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule ComplexScriptSize par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionCharacter** <br/> |
|Index de la ligne :  <br/> |**visRowCharacter** +  *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visCharacterComplexScriptSize** <br/> |
   

