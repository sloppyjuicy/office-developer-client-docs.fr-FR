---
title: CenterY, cellule (section Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033792
ms.localizationpriority: medium
ms.assetid: 7ce0bf66-dc8b-9646-7b04-50c969ecd67a
description: Détermine si la page de dessin est centrée verticalement sur la page d'impression.
ms.openlocfilehash: b72acb3db2a56ab44da92dd30a3f748941ca7fbe
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578024"
---
# <a name="centery-cell-print-properties-section"></a>CenterY, cellule (section Print Properties)

Détermine si la page de dessin est centrée verticalement sur la page d'impression. 
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | Centre la page de dessin verticalement sur la page d'impression.  <br/> |
| FALSE  <br/> | Ne centre pas la page de dessin verticalement sur la page d'impression (valeur par défaut).  <br/> |
   
## <a name="remarks"></a>Remarques

Par défaut, les pages de dessins sont alignées sur le haut et la gauche de la page d'impression. Définir les cellules CenterX et CenterY sur TRUE place la page de dessin au centre de la page d'impression (ou les pages lorsque la mosaïque est nécessaire). 
  
Pour obtenir une référence à la cellule CenterY par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | CenterY  <br/> |
   
Pour obtenir une référence à la cellule CenterY à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowPrintProperties** <br/> |
| Index de la cellule :  <br/> |**visPrintPropertiesCenterY** <br/> |
   

