---
title: PrintPageOrientation, cellule (section Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033795
ms.localizationpriority: medium
ms.assetid: f8354d0d-0ce2-fb33-ddf7-611a2c24a8be
description: Détermine si la page est imprimée en orientation portrait ou paysage.
ms.openlocfilehash: b197b89439b6f2c4cacafee86d5237c7de77d97c
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63628403"
---
# <a name="printpageorientation-cell-print-properties-section"></a>PrintPageOrientation, cellule (section Print Properties)

Détermine si la page est imprimée en orientation portrait ou paysage.
  
|**Valeur**|**Orientation**|**Constante d'automation**|
|:-----|:-----|:-----|
| 0  <br/> | Identique au papier de l'imprimante  <br/> |**visPPOSameAsPrinter** <br/> |
| 1  <br/> | Portrait  <br/> |**visPPOPortrait** <br/> |
|2  <br/> |Paysage  <br/> |**visPPOLandscape** <br/> |
   
## <a name="remarks"></a>Remarques

Lorsque vous insérez de nouvelles pages dans un document, ce paramètre est par défaut le paramètre de la page active.
  
Pour obtenir une référence à la cellule PrintPageOrientation par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de la cellule :**  <br/> | PrintPageOrientation  <br/> |
   
Pour obtenir une référence à la cellule PrintPageOrientation à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowPrintProperties** <br/> |
| **Index de la cellule :**  <br/> |**visPrintPropertiesPageOrientation** <br/> |
   

