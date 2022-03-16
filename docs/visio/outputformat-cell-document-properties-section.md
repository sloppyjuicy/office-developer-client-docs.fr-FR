---
title: OutputFormat, cellule (section Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251617
ms.localizationpriority: medium
ms.assetid: 17238019-c800-5d3a-32f6-fb0008d4e25f
description: Détermine le format de sortie d'un dessin. Les pages de dessin sont généralement mises en forme pour l'impression (par défaut), mais vous pouvez choisir d'autres formats de sortie.
ms.openlocfilehash: 4b01a066c3b516af2d21799b3a05fb74e0f88017
ms.sourcegitcommit: b2c5a02b2d0abd2da2542089fc3f83ff07e121e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2022
ms.locfileid: "63507246"
---
# <a name="outputformat-cell-document-properties-section"></a>OutputFormat, cellule (section Document Properties)

Détermine le format de sortie d'un dessin. Les pages de dessin sont généralement mises en forme pour l'impression (par défaut), mais vous pouvez choisir d'autres formats de sortie.
  
|**Valeur**|**Format de sortie**|
|:-----|:-----|
| 0  <br/> | Impression (par défaut)  <br/> |
| 1  <br/> | Diaporama PowerPoint  <br/> |
| 2  <br/> | Sortie HTML ou GIF  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule OutputFormat par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de la cellule :**  <br/> | OutputFormat  <br/> |
   
Pour obtenir une référence à la cellule OutputFormat à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowDoc** <br/> |
| **Index de la cellule :**  <br/> |**visDocOutputFormat** <br/> |
   

