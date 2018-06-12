---
title: InhibitSnap, cellule (section Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251620
localization_priority: Normal
ms.assetid: ab9fcebc-1550-3b9e-e3b4-e8b92424390b
description: Détermine si les formes d'une page en premier plan s'alignent sur d'autres objets de la page et sur des formes de la page d'arrière-plan.
ms.openlocfilehash: b95dafda9ebef36db34f60585ab3ed2164ade415
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788831"
---
# <a name="inhibitsnap-cell-page-properties-section"></a>InhibitSnap, cellule (section Page Properties)

Détermine si les formes d'une page en premier plan s'alignent sur d'autres objets de la page et sur des formes de la page d'arrière-plan.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | Interdit tout alignement sur la page à l'exception de l'alignement sur la règle et sur la grille.  <br/> |
| FALSE  <br/> | Active l'alignement.  <br/> |
   
## <a name="remarks"></a>Notes

Pour obtenir une référence à la cellule InhibitSnap par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | InhibitSnap  <br/> |
   
Pour obtenir une référence à la cellule InhibitSnap par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowPage** <br/> |
| Index de la cellule :  <br/> |**visPageInhibitSnap** <br/> |
   

