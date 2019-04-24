---
title: CtrlAsInput, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1225
localization_priority: Normal
ms.assetid: c6fd0aba-7c33-b77f-207b-ba704b3e0756
description: Détermine la forme parente lors de la manipulation de formes avec des poignées de contrôle. Cette cellule définit le comportement de toutes les formes de la page de dessin.
ms.openlocfilehash: a530c48156043bec0cd58d79aead1a403c17ddce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282907"
---
# <a name="ctrlasinput-cell-page-layout-section"></a>CtrlAsInput, cellule (section Page Layout)

Détermine la forme parente lors de la manipulation de formes avec des poignées de contrôle. Cette cellule définit le comportement de toutes les formes de la page de dessin.
  
|**Value**|**Description**|
|:-----|:-----|
| TRUE  <br/> | Définit la forme à laquelle la poignée de contrôle est liée comme parent.  <br/> |
| FALSE  <br/> | Valeur par défaut. Définit la forme contenant la poignée de contrôle comme parent.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule CtrlAsInput par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | CtrlAsInput  <br/> |
   
Pour obtenir une référence à la cellule CtrlAsInput à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowPageLayout** <br/> |
| Index de la cellule :  <br/> |**visPLOCtrlAsInput** <br/> |
   

