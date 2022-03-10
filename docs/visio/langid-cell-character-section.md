---
title: LangID, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033769
ms.localizationpriority: medium
ms.assetid: c68289b8-ef45-9e1e-12ae-6613587e4990
description: Indique la langue dans laquelle le texte a été entré.
ms.openlocfilehash: 1e9c1e7dbe1fb5929f784f74333aa66e9b5aad1e
ms.sourcegitcommit: 4164855836af53a068bbbc5b5d126f83ee83e324
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2022
ms.locfileid: "63427160"
---
# <a name="langid-cell-character-section"></a>LangID, cellule (section Character)

Indique la langue dans laquelle le texte a été entré. 
  
## <a name="remarks"></a>Remarques

Pour une liste des langues prises en charge par les applications Microsoft Office, reportez-vous à la rubrique [DocLangID](doclangid-cell-document-properties-section.md) (section Document Properties). 
  
Pour obtenir une référence à la cellule LangID par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | Char.LangID[  *i*  ] où  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule LangID à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionCharacter** <br/> |
| **Index de la ligne :**  <br/> |**visRowCharacter** +   *i* où *i* = 0, 1, 2... |
| **Index de la cellule :**  <br/> |**visCharacterLangID** <br/> |
   

