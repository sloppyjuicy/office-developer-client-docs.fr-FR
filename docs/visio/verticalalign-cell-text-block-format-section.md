---
title: VerticalAlign, cellule (section Text Block Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1105
ms.localizationpriority: medium
ms.assetid: ff34a23b-2881-864f-42e4-871c4fde0992
description: Détermine l'alignement vertical du texte dans le bloc de texte.
ms.openlocfilehash: effb1980c6bd8425cd6906e285fa0a6b79495198
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63520167"
---
# <a name="verticalalign-cell-text-block-format-section"></a>VerticalAlign, cellule (section Text Block Format)

Détermine l'alignement vertical du texte dans le bloc de texte.
  
|**Valeur**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
| 0  <br/> | Haut  <br/> |**visVertTop** <br/> |
| 1  <br/> | Milieu  <br/> |**visVertMiddle** <br/> |
| 2  <br/> | Bas  <br/> |**visVertBottom** <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule VerticalAlign par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de la cellule :**  <br/> | VerticalAlign  <br/> |
   
Pour obtenir une référence à la cellule VerticalAlign par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowText** <br/> |
| **Index de la cellule :**  <br/> |**visTxtBlkVerticalAlign** <br/> |
   

