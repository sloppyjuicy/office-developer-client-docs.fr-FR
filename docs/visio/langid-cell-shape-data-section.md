---
title: LangID, cellule (section Shape Data)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033771
localization_priority: Normal
ms.assetid: 6bd2781a-d4e7-136f-8996-62ebc5f890ab
description: Indique la langue dans laquelle les données forme ont été entrées.
ms.openlocfilehash: 696c42483390509474eb82bd8cc0046beee345e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788920"
---
# <a name="langid-cell-shape-data-section"></a>LangID, cellule (section Shape Data)

Indique la langue dans laquelle les données forme ont été entrées. 
  
## <a name="remarks"></a>Notes

Pour obtenir la liste des langues prises en charge par les applications Microsoft Office System, reportez-vous à la cellule [DocLangID](doclangid-cell-document-properties-section.md) (Section Document Properties). 
  
Pour obtenir une référence à la cellule LangID par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Propriétés.  *nom* . LangID où de propriétés.  *Name* est le nom de ligne  <br/> |
   
Pour obtenir une référence à la cellule LangID par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionProp** <br/> |
| Index de la ligne :  <br/> |**visRowProp** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visCustPropsLangID** <br/> |
   

