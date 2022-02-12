---
title: ComplexScriptFont, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60034
ms.localizationpriority: medium
ms.assetid: e1cf9e97-101b-384f-65fe-0169c89dfccc
description: Contient le numéro de la police utilisée pour mettre en forme du texte composé de caractères de script complexe. Les numéros de police varient en fonction des polices installées sur votre système.
ms.openlocfilehash: d8da0262df8780ba078b304a46311fa8756dd994
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62772885"
---
# <a name="complexscriptfont-cell-character-section"></a>ComplexScriptFont, cellule (section Character)

Contient le numéro de la police utilisée pour mettre en forme du texte composé de caractères de script complexe. Les numéros de police varient en fonction des polices installées sur votre système. 
  
## <a name="remarks"></a>Remarques

Les tailles de police de script complexes  sont répertoriées sous  l’onglet Police dans la boîte de dialogue  Texte (cliquez sur la flèche du groupe Police sous **l’onglet Accueil**). Cette liste apparaît uniquement si vous avez ajouté une langue qui contient des caractères asiatiques ou des caractères de script complexe dans la boîte de dialogue **Préférences de langue Microsoft Office**. (Cliquez sur **Démarrer**, cliquez sur **Tous les programmes**, cliquez sur **Microsoft Office**, cliquez sur **Outils Microsoft Office**, puis cliquez sur **Préférences de langue Microsoft Office**.
  
Le numéro 0 (zéro) signifie qu'aucune police n'est spécifiée. La police Latin ou les polices par défaut sont utilisées.
  
Pour obtenir une référence à la cellule ComplexScriptSize par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |Char.ComplexScriptFont[ *i*  ] où  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule ComplexScriptFont à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionCharacter** <br/> |
|Index de la ligne :  <br/> |**visRowCharacter** +   *i* où *i* = 0, 1, 2... |
|Index de la cellule :  <br/> |**visCharacterComplexScriptFont** <br/> |
   

