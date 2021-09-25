---
title: QuickStyleLineColor Cell (Quick Style Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: dcfb792f-e02a-4059-acec-a178d221097c
description: Détermine la couleur de thème que la ligne d’une forme utilise, sous la forme d’un nombre integer de 0 à 7.
ms.openlocfilehash: 2ebcb23a308ef1c28a87860e9d75bb832e87bba1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623158"
---
# <a name="quickstylelinecolor-cell-quick-style-section"></a>QuickStyleLineColor Cell (Quick Style Section)

Détermine la couleur de thème que la ligne d’une forme utilise, sous la forme d’un nombre integer de 0 à 7.
  
|||
|:-----|:-----|
|Valeur  <br/> |Description  <br/> |
|0  <br/> |La couleur de trait de forme hérite de la couleur de thème Foncé.  <br/> |
|1  <br/> |La couleur de trait de forme hérite de la couleur de thème Clair.  <br/> |
|2  <br/> |La couleur de trait de forme hérite de la couleur de thème Accent 1  <br/> |
|3  <br/> |La couleur de trait de forme hérite de la couleur de thème Accent 2  <br/> |
|4   <br/> |La couleur de trait de forme hérite de la couleur de thème Accent 3  <br/> |
|5  <br/> |La couleur de trait de forme hérite de la couleur de thème Accent 4  <br/> |
|6   <br/> |La couleur de trait de forme hérite de la couleur de thème Accent 5  <br/> |
|7   <br/> |La couleur de trait de forme hérite de la couleur de thème Accent 6  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **QuickStyleLineColor** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU,** utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | QuickStyleLineColor  <br/> |
   
Pour obtenir une référence à la **cellule QuickStyleLineColor** à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowQuickStyleProperties** <br/> |
| Index de la cellule :  <br/> |**visQuickStyleLineColor** <br/> |
   

