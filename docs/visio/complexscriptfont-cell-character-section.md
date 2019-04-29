---
title: ComplexScriptFont, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60034
localization_priority: Normal
ms.assetid: e1cf9e97-101b-384f-65fe-0169c89dfccc
description: Contient le numéro de la police utilisée pour mettre en forme du texte composé de caractères de script complexe. Les numéros de police varient en fonction des polices installées sur votre système.
ms.openlocfilehash: 5ec8deb59b875a01592b6d7b652204089ecf11e0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404833"
---
# <a name="complexscriptfont-cell-character-section"></a>ComplexScriptFont, cellule (section Character)

Contient le numéro de la police utilisée pour mettre en forme du texte composé de caractères de script complexe. Les numéros de police varient en fonction des polices installées sur votre système. 
  
## <a name="remarks"></a>Remarques

Les tailles de police de script complexe sont répertoriées sous l'onglet **police** de la boîte de dialogue **texte** (cliquez sur la flèche dans le groupe **police** de l'onglet **Accueil** ). Cette liste apparaît uniquement si vous avez ajouté une langue qui contient des caractères asiatiques ou des caractères de script complexe dans la boîte de dialogue **Préférences de langue Microsoft Office**. (Cliquez sur **Démarrer**, cliquez sur **Tous les programmes**, cliquez sur **Microsoft Office**, cliquez sur **Outils Microsoft Office**, puis cliquez sur **Préférences de langue Microsoft Office**.
  
Le numéro 0 (zéro) signifie qu'aucune police n'est spécifiée. La police Latin ou les polices par défaut sont utilisées.
  
Pour obtenir une référence à la cellule ComplexScriptSize par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |Char. ComplexScriptFont [ *i* ] où *i* = <1>, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule ComplexScriptFont à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionCharacter** <br/> |
|Index de la ligne :  <br/> |**visRowCharacter** +  *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visCharacterComplexScriptFont** <br/> |
   

