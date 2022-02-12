---
title: QuickStyleFontColor Cell (Quick Style Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 31c56d08-19ea-4b8b-8be7-42e1c736fbca
description: Détermine la couleur de police des styles rapides dont le texte d’une forme hérite du thème actif, sous la forme d’un nombre integer de 0 à 1.
ms.openlocfilehash: 3b3b73d060bf2a2d83c8b8461faad0aa1119eaf3
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62788793"
---
# <a name="quickstylefontcolor-cell-quick-style-section"></a>QuickStyleFontColor Cell (Quick Style Section)

Détermine la couleur de police des styles rapides dont le texte d’une forme hérite du thème actif, sous la forme d’un nombre integer de 0 à 1. 
  
|||
|:-----|:-----|
|Valeur  <br/> |Description  <br/> |
|0  <br/> |Le texte de la forme utilise la couleur de police Foncé. |
|1  <br/> |Le texte de la forme utilise la couleur de police Light. |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **QuickStyleFontColor** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | QuickStyleFontColor  <br/> |
   
Pour obtenir une référence à la **cellule QuickStyleFontColor** à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowQuickStyleProperties** <br/> |
| Index de la cellule :  <br/> |**visQuickStyleFontColor** <br/> |
   

