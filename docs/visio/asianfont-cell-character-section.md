---
title: AsianFont, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033764
localization_priority: Normal
ms.assetid: 45bfaaaa-52cc-f8b4-68e7-8b99e5788ce1
description: Contient le numéro de la police utilisée pour mettre en forme le texte comportant des caractères asiatiques. Les numéros de police varient en fonction des polices installées sur votre système.
ms.openlocfilehash: 1fbaa0b27a0c639519c302129142dcefe5708115
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788024"
---
# <a name="asianfont-cell-character-section"></a>AsianFont, cellule (section Character)

Contient le numéro de la police utilisée pour mettre en forme le texte comportant des caractères asiatiques. Les numéros de police varient en fonction des polices installées sur votre système. 
  
## <a name="remarks"></a>Note

Les polices asiatiques sont répertoriées sous l’onglet **police** de la boîte de dialogue **texte** (cliquez sur la flèche dans la **police** de groupe sous l’onglet **accueil** ). Cette liste apparaît uniquement si vous avez ajouté une langue qui contienne des caractères asiatiques ou à script complexe, dans la boîte de dialogue **Préférences linguistiques de Microsoft Office** . (Cliquez sur **Démarrer**, sur **Tous les programmes**, sur **Microsoft Office**, sur **Outils Microsoft Office**, puis cliquez sur **Préférences linguistiques de Microsoft Office**.
  
Le numéro 0 signifie qu'aucune police n'est spécifiée. La police Latin ou les polices par défaut sont utilisées si elles contiennent les caractères nécessaires.
  
Pour obtenir une référence à la cellule AsianFont par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |Char.AsianFont [ *i* ] où *i* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule AsianFont par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionCharacter** <br/> |
|Index de la ligne :  <br/> |**visRowCharacter** +  *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visCharacterAsianFont** <br/> |
   

