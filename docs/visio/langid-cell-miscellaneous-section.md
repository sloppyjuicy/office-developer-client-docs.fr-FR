---
title: LangID, cellule (section Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60051
localization_priority: Normal
ms.assetid: 815e0df8-5ebf-ef1b-d620-bce8abb69f1a
description: Indique la langue dans laquelle les formules de la cellule ont été créées.
ms.openlocfilehash: 669bde032daeda90b22cdab5d1758c6cbd4109d5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788940"
---
# <a name="langid-cell-miscellaneous-section"></a>LangID, cellule (section Miscellaneous)

Indique la langue dans laquelle les formules de la cellule ont été créées. 
  
## <a name="remarks"></a>Notes

Pour obtenir la liste des langues prises en charge par les applications Microsoft Office, consultez la rubrique de la cellule (Section Document Properties) [DocLangID](doclangid-cell-document-properties-section.md) . 
  
Pour obtenir une référence à la cellule LangID par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | ID de langue  <br/> |
   
Pour obtenir une référence à la cellule LangID par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowMisc** <br/> |
| Index de la cellule :  <br/> |**visObjLangID** <br/> |
   

