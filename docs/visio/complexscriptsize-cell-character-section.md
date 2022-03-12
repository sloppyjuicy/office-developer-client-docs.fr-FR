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
ms.openlocfilehash: a0282a4f25ddab2c60b5c6e05e4e9e1d2ae47219
ms.sourcegitcommit: 7b410a51d1e8c97e9cce8d4aa75074162b7d9485
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/12/2022
ms.locfileid: "63448369"
---
# <a name="complexscriptsize-cell-character-section"></a>ComplexScriptSize, cellule (section Character)

Taille de la police utilisée pour mettre en forme du texte composé de caractères de script complexe. 
  
## <a name="remarks"></a>Remarques

Les tailles de police de script complexes  sont répertoriées sous  l’onglet Police dans la boîte de dialogue  Texte (cliquez sur la flèche du groupe Police sous **l’onglet Accueil**). Cette liste apparaît uniquement si vous avez ajouté une langue qui contient des caractères asiatiques ou des caractères de script complexe dans la boîte de dialogue **Préférences de langue Microsoft Office**. (Cliquez sur **Démarrer**, cliquez sur **Tous les programmes**, cliquez sur **Microsoft Office**, cliquez sur **Outils Microsoft Office**, puis cliquez sur **Préférences de langue Microsoft Office**.
  
Vous pouvez entrer cette valeur comme taille de point explicite ou comme pourcentage. Si vous indiquez un pourcentage, la valeur est basée sur celle de la cellule Size. Une valeur par défaut de 0 (zéro) signifie 100 %. 
  
Pour obtenir une référence à la cellule ComplexScriptSize par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de cellule :**  <br/> |Char.ComplexScriptSize[ *i*  ] où  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule ComplexScriptSize à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionCharacter** <br/> |
|**Index de la ligne :**  <br/> |**visRowCharacter** +   *i* où *i* = 0, 1, 2... |
|**Index de la cellule :**  <br/> |**visCharacterComplexScriptSize** <br/> |
   

