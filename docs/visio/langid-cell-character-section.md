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
ms.openlocfilehash: e1f244d6d8e31201576a9a88ace9701814b0e0a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419281"
---
# <a name="langid-cell-character-section"></a>LangID, cellule (section Character)

Indique la langue dans laquelle le texte a été entré. 
  
## <a name="remarks"></a>Remarques

Pour une liste des langues prises en charge par les applications Microsoft Office, reportez-vous à la rubrique [DocLangID](doclangid-cell-document-properties-section.md) (section Document Properties). 
  
Pour obtenir une référence à la cellule LangID par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Char.LangID[  *i*  ] où  *i*  = <1>, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule LangID à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionCharacter** <br/> |
| Index de la ligne :  <br/> |**visRowCharacter**  +   *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visCharacterLangID** <br/> |
   

