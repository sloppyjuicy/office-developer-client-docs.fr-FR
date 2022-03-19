---
title: QuickStyleFontColor Cell (Quick Style Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 31c56d08-19ea-4b8b-8be7-42e1c736fbca
description: Détermine la couleur de police des styles rapides dont le texte d’une forme hérite du thème actif, sous la forme d’un nombre integer de 0 à 1.
ms.openlocfilehash: 3b90edfdd8e29e252f32895639373279cf3360aa
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63627080"
---
# <a name="quickstylefontcolor-cell-quick-style-section"></a>QuickStyleFontColor Cell (Quick Style Section)

Détermine la couleur de police des styles rapides dont le texte d’une forme hérite du thème actif, sous la forme d’un nombre integer de 0 à 1. 
  
|Valeur  <br/> |Description  <br/> |
|:-----|:-----|
|0  <br/> |Le texte de la forme utilise la couleur de police Foncé. |
|1  <br/> |Le texte de la forme utilise la couleur de police Light. |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **QuickStyleFontColor** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | QuickStyleFontColor  <br/> |
   
Pour obtenir une référence à la **cellule QuickStyleFontColor** à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowQuickStyleProperties** <br/> |
| **Index de la cellule :**  <br/> |**visQuickStyleFontColor** <br/> |
   

