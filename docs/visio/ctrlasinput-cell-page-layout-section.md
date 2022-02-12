---
title: CtrlAsInput, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1225
ms.localizationpriority: medium
ms.assetid: c6fd0aba-7c33-b77f-207b-ba704b3e0756
description: Détermine la forme parente lors de la manipulation de formes avec des poignées de contrôle. Cette cellule définit le comportement de toutes les formes de la page de dessin.
ms.openlocfilehash: aafe53a8e1e5154dd391380049b0d6e3235ea2d4
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62774446"
---
# <a name="ctrlasinput-cell-page-layout-section"></a>CtrlAsInput, cellule (section Page Layout)

Détermine la forme parente lors de la manipulation de formes avec des poignées de contrôle. Cette cellule définit le comportement de toutes les formes de la page de dessin.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | Définit la forme à laquelle la poignée de contrôle est liée comme parent. |
| FALSE  <br/> | Valeur par défaut. Définit la forme contenant la poignée de contrôle comme parent. |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule CtrlAsInput par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | CtrlAsInput  <br/> |
   
Pour obtenir une référence à la cellule CtrlAsInput à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowPageLayout** <br/> |
| Index de la cellule :  <br/> |**visPLOCtrlAsInput** <br/> |
   

