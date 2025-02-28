---
title: LangID, cellule (section Shape Data)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033771
ms.localizationpriority: medium
ms.assetid: 6bd2781a-d4e7-136f-8996-62ebc5f890ab
description: Indique la langue dans laquelle les données forme ont été entrées.
ms.openlocfilehash: a233734577d60baff7ab7aece2f45cfeb1ba27d6
ms.sourcegitcommit: 4164855836af53a068bbbc5b5d126f83ee83e324
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2022
ms.locfileid: "63426642"
---
# <a name="langid-cell-shape-data-section"></a>LangID, cellule (section Shape Data)

Indique la langue dans laquelle les données forme ont été entrées. 
  
## <a name="remarks"></a>Remarques

Pour une liste des langues prises en charge par les applications du système Microsoft Office, reportez-vous à la cellule [DocLangID](doclangid-cell-document-properties-section.md) (section Document Properties). 
  
Pour obtenir une référence à la cellule LangID par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | Prop.  *nom*  . LangID où Prop.  *nom est*  le nom de ligne  <br/> |
   
Pour obtenir une référence à la cellule LangID à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionProp** <br/> |
| **Index de la ligne :**  <br/> |**visRowProp** +   *i* où *i* = 0, 1, 2... |
| **Index de la cellule :**  <br/> |**visCustPropsLangID** <br/> |
   

