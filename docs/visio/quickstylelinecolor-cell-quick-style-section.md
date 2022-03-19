---
title: QuickStyleLineColor Cell (Quick Style Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: dcfb792f-e02a-4059-acec-a178d221097c
description: Détermine la couleur de thème que la ligne d’une forme utilise, sous la forme d’un nombre integer de 0 à 7.
ms.openlocfilehash: a8c279477885fb956dba95a3ff667a8040bc198d
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63633770"
---
# <a name="quickstylelinecolor-cell-quick-style-section"></a>QuickStyleLineColor Cell (Quick Style Section)

Détermine la couleur de thème que la ligne d’une forme utilise, sous la forme d’un nombre integer de 0 à 7.
  
|Valeur  <br/> |Description  <br/> |
|:-----|:-----|
|0  <br/> |La couleur de trait de forme hérite de la couleur de thème Foncé. |
|1  <br/> |La couleur du trait de forme hérite de la couleur de thème Clair. |
|2  <br/> |La couleur de trait de forme hérite de la couleur de thème Accent 1  <br/> |
|3  <br/> |La couleur de trait de forme hérite de la couleur de thème Accent 2  <br/> |
|4  <br/> |La couleur de trait de forme hérite de la couleur de thème Accent 3  <br/> |
|5  <br/> |La couleur de trait de forme hérite de la couleur de thème Accent 4  <br/> |
|6   <br/> |La couleur de trait de forme hérite de la couleur de thème Accent 5  <br/> |
|7   <br/> |La couleur de trait de forme hérite de la couleur de thème Accent 6  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **QuickStyleLineColor** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | QuickStyleLineColor  <br/> |
   
Pour obtenir une référence à la **cellule QuickStyleLineColor** à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowQuickStyleProperties** <br/> |
| **Index de la cellule :**  <br/> |**visQuickStyleLineColor** <br/> |
   

