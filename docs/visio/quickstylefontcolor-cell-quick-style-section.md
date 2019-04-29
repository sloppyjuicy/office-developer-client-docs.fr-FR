---
title: QuickStyleFontColor Cell (Quick Style Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31c56d08-19ea-4b8b-8be7-42e1c736fbca
description: Détermine la couleur de la police à partir des styles rapides hérités par le texte d'une forme à partir du thème actif, sous la forme d'un nombre entier compris entre 0-1.
ms.openlocfilehash: bd645383df02260fcf6a2045764d9a1b44126090
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415025"
---
# <a name="quickstylefontcolor-cell-quick-style-section"></a>QuickStyleFontColor Cell (Quick Style Section)

Détermine la couleur de la police à partir des styles rapides hérités par le texte d'une forme à partir du thème actif, sous la forme d'un nombre entier compris entre 0-1. 
  
|||
|:-----|:-----|
|Valeur  <br/> |Description  <br/> |
|0  <br/> |Le texte de la forme utilise la couleur de la police foncée.  <br/> |
|0,1  <br/> |Le texte de la forme utilise la couleur de la police claire.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **QuickStyleFontColor** par un nom à partir d'une autre formule, par valeur de l'attribut **N** d'un élément de **cellule** ou d'un programme en faisant appel à la propriété **CellsU** , utilisez: 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | QuickStyleFontColor  <br/> |
   
Pour obtenir une référence à la cellule **QuickStyleFontColor** à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants: 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowQuickStyleProperties** <br/> |
| Index de la cellule :  <br/> |**visQuickStyleFontColor** <br/> |
   

