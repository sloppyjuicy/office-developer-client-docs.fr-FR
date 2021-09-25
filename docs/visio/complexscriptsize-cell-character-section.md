---
title: ComplexScriptSize, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033768
ms.localizationpriority: medium
ms.assetid: f58687d7-2ba4-ff77-0bcc-3106867d89de
description: Taille de la police utilisée pour mettre en forme du texte composé de caractères de script complexe.
ms.openlocfilehash: 8d810cecb7f9bd1d80895892a362d808f8adc3f7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608472"
---
# <a name="complexscriptsize-cell-character-section"></a>ComplexScriptSize, cellule (section Character)

Taille de la police utilisée pour mettre en forme du texte composé de caractères de script complexe. 
  
## <a name="remarks"></a>Remarques

Les tailles de police de script  complexes sont répertoriées sous  l’onglet Police de la boîte de dialogue Texte (cliquez sur la flèche du groupe Police sous **l’onglet Accueil).**  Cette liste apparaît uniquement si vous avez ajouté une langue qui contient des caractères asiatiques ou des caractères de script complexe dans la boîte de dialogue **Préférences de langue Microsoft Office**. (Cliquez sur **Démarrer**, cliquez sur **Tous les programmes**, cliquez sur **Microsoft Office**, cliquez sur **Outils Microsoft Office**, puis cliquez sur **Préférences de langue Microsoft Office**.
  
Vous pouvez entrer cette valeur comme taille de point explicite ou comme pourcentage. Si vous indiquez un pourcentage, la valeur est basée sur celle de la cellule Size. Une valeur par défaut de 0 (zéro) signifie 100 %. 
  
Pour obtenir une référence à la cellule ComplexScriptSize par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |Char.ComplexScriptSize[ *i*  ] où  *i*  = <1>, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule ComplexScriptSize à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionCharacter** <br/> |
|Index de la ligne :  <br/> |**visRowCharacter**  +   *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visCharacterComplexScriptSize** <br/> |
   

