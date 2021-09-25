---
title: InhibitSnap, cellule (section Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251620
ms.localizationpriority: medium
ms.assetid: ab9fcebc-1550-3b9e-e3b4-e8b92424390b
description: Détermine si les formes d'une page en premier plan s'alignent sur d'autres objets de la page et sur des formes de la page d'arrière-plan.
ms.openlocfilehash: c559bb97357e75508b8c1da742d970262f0ef6f9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628079"
---
# <a name="inhibitsnap-cell-page-properties-section"></a>InhibitSnap, cellule (section Page Properties)

Détermine si les formes d'une page en premier plan s'alignent sur d'autres objets de la page et sur des formes de la page d'arrière-plan.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | Interdit tout alignement sur la page à l'exception de l'alignement sur la règle et sur la grille.  <br/> |
| FALSE  <br/> | Active l'alignement.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule InhibitSnap par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | InhibitSnap  <br/> |
   
Pour obtenir une référence à la cellule InhibitSnap à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowPage** <br/> |
| Index de la cellule :  <br/> |**visPageInhibitSnap** <br/> |
   

