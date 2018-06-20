---
title: PrintPageOrientation, cellule (section Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033795
localization_priority: Normal
ms.assetid: f8354d0d-0ce2-fb33-ddf7-611a2c24a8be
description: Détermine si la page est imprimée en orientation portrait ou paysage.
ms.openlocfilehash: 2adc7dadcb3702e6c5307bb569b2ae1df7aee54e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789361"
---
# <a name="printpageorientation-cell-print-properties-section"></a>PrintPageOrientation, cellule (section Print Properties)

Détermine si la page est imprimée en orientation portrait ou paysage.
  
|**Valeur**|**Orientation**|**Constante d’Automation**|
|:-----|:-----|:-----|
| 0  <br/> | Identique au papier de l'imprimante  <br/> |**visPPOSameAsPrinter** <br/> |
| 1  <br/> | Portrait  <br/> |**visPPOPortrait** <br/> |
|2  <br/> |Paysage  <br/> |**visPPOLandscape** <br/> |
   
## <a name="remarks"></a>Remarques

Lorsque vous insérez de nouvelles pages dans un document, ce paramètre par défaut pour le paramètre dans la page active.
  
Pour obtenir une référence à la cellule PrintPageOrientation par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | PrintPageOrientation  <br/> |
   
Pour obtenir une référence à la cellule PrintPageOrientation par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowPrintProperties** <br/> |
| Index de la cellule :  <br/> |**visPrintPropertiesPageOrientation** <br/> |
   

