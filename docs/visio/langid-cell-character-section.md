---
title: LangID, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033769
localization_priority: Normal
ms.assetid: c68289b8-ef45-9e1e-12ae-6613587e4990
description: Indique la langue dans laquelle le texte a été entré.
ms.openlocfilehash: e503abb2365635fa25a4dbec54b7fe3da4043fa8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788897"
---
# <a name="langid-cell-character-section"></a>LangID, cellule (section Character)

Indique la langue dans laquelle le texte a été entré. 
  
## <a name="remarks"></a>Notes

Pour obtenir la liste des langues prises en charge par les applications Microsoft Office, consultez la rubrique de la cellule (Section Document Properties) [DocLangID](doclangid-cell-document-properties-section.md) . 
  
Pour obtenir une référence à la cellule LangID par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Char.LangID [ *i* ] où *i* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule LangID par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionCharacter** <br/> |
| Index de la ligne :  <br/> |**visRowCharacter** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visCharacterLangID** <br/> |
   

