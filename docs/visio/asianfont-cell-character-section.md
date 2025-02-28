---
title: AsianFont, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033764
ms.localizationpriority: medium
ms.assetid: 45bfaaaa-52cc-f8b4-68e7-8b99e5788ce1
description: Contient le numéro de la police utilisée pour mettre en forme le texte comportant des caractères asiatiques. Les numéros de police varient en fonction des polices installées sur votre système.
ms.openlocfilehash: 2aaeea4dffbe78868897548dd3f09d44c5e311ad
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63406259"
---
# <a name="asianfont-cell-character-section"></a>AsianFont, cellule (section Character)

Contient le numéro de la police utilisée pour mettre en forme le texte comportant des caractères asiatiques. Les numéros de police varient en fonction des polices installées sur votre système. 
  
## <a name="remarks"></a>Remarques

Les polices asiatiques sont répertoriées sous l’onglet **Police** dans la boîte de dialogue **Texte** (cliquez sur la flèche dans le groupe **Police** sous l’onglet **Accueil**). Cette liste apparaît uniquement si vous avez ajouté une langue qui contient des caractères asiatiques ou des caractères de script complexe dans la boîte de dialogue **Préférences de langue Microsoft Office**. (Cliquez sur **Démarrer**, cliquez sur **Tous les programmes**, cliquez sur **Microsoft Office**, cliquez sur **Outils Microsoft Office**, puis cliquez sur **Préférences de langue Microsoft Office**.
  
Le numéro 0 signifie qu'aucune police n'est spécifiée. La police Latin ou les polices par défaut sont utilisées si elles contiennent les caractères nécessaires.
  
Pour obtenir une référence à la cellule AsianFont par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de cellule :**  <br/> |Char.AsianFont[ *i*  ] où  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule AsianFont à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionCharacter** <br/> |
|**Index de la ligne :**  <br/> |**visRowCharacter** +   *i* où *i* = 0, 1, 2... |
|**Index de la cellule :**  <br/> |**visCharacterAsianFont** <br/> |
   

