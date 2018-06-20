---
title: QuickStyleLineColor, cellule (Section Style rapide)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dcfb792f-e02a-4059-acec-a178d221097c
description: Détermine quel couleur de thème utilise de trait d’une forme, comme un entier compris entre 0 et 7.
ms.openlocfilehash: 2a660472998ade8148e8b70a3c6e4fc5fb3f4820
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789399"
---
# <a name="quickstylelinecolor-cell-quick-style-section"></a>QuickStyleLineColor, cellule (Section Style rapide)

Détermine quel couleur de thème utilise de trait d’une forme, comme un entier compris entre 0 et 7.
  
|||
|:-----|:-----|
|Valeur  <br/> |Description  <br/> |
|0  <br/> |La couleur de trait forme hérite de la couleur de thème foncé.  <br/> |
|1  <br/> |La couleur de trait forme hérite de la couleur de thème clair.  <br/> |
|2  <br/> |La couleur de trait forme hérite de la couleur de thème Accent 1  <br/> |
|3  <br/> |La couleur de trait forme hérite de la couleur de thème Accent 2  <br/> |
|4  <br/> |La couleur de trait forme hérite de la couleur de thème Accent 3  <br/> |
|5  <br/> |La couleur de trait forme hérite de la couleur de thème Accent 4  <br/> |
|6  <br/> |La couleur de trait forme hérite de la couleur de thème Accent 5  <br/> |
|7  <br/> |La couleur de trait forme hérite de la couleur de thème Accent 6  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **QuickStyleLineColor** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | QuickStyleLineColor  <br/> |
   
Pour obtenir une référence à la cellule **QuickStyleLineColor** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowQuickStyleProperties** <br/> |
| Index de la cellule :  <br/> |**visQuickStyleLineColor** <br/> |
   

