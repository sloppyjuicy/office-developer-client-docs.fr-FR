---
title: HideForApply, cellule (section Style Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251698
ms.localizationpriority: medium
ms.assetid: 62d87db9-b8ca-60b6-bf27-5168c718ec96
description: Détermine l’endroit où un style est affiché dans l’interface utilisateur Visio Microsoft.
ms.openlocfilehash: 43938ea5521928231cb3d082ff028cafeb74675b
ms.sourcegitcommit: b2c5a02b2d0abd2da2542089fc3f83ff07e121e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2022
ms.locfileid: "63506882"
---
# <a name="hideforapply-cell-style-properties-section"></a>HideForApply, cellule (section Style Properties)

Détermine l’endroit où un style est affiché dans l’interface utilisateur Visio Microsoft.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | Le style n’apparaît que dans l’**Explorateur de dessins**. |
| FALSE  <br/> | Le style apparaît dans l’**Explorateur de dessins**. |
   
## <a name="remarks"></a>Remarques

Lorsque vous basez un nouveau style sur un style masqué, il n'hérite pas de cet attribut.
  
Pour obtenir une référence à la cellule HideForApply par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | HideForApply  <br/> |
   
Pour obtenir une référence à la cellule HideForApply à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowStyle** <br/> |
| **Index de la cellule :**  <br/> |**visStyleHidden** <br/> |
   

