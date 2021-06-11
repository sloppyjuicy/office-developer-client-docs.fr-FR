---
title: ConLineJumpDirX, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm185
localization_priority: Normal
ms.assetid: f0671835-8d48-907a-eca6-43953658f800
description: Détermine la direction de la déviation du trait dans le cas d'un connecteur dynamique horizontal d'une forme.
ms.openlocfilehash: 22b9366b750a85a76498b83880aac2b9b974e1ac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415039"
---
# <a name="conlinejumpdirx-cell-shape-layout-section"></a>ConLineJumpDirX, cellule (section Shape Layout)

Détermine la direction de la déviation du trait dans le cas d'un connecteur dynamique horizontal d'une forme.
  
|**Valeur**|**Direction du saut de ligne**|**Constante d'automation**|
|:-----|:-----|:-----|
| 0  <br/> | Valeur par défaut de la page  <br/> |**visLOJumpDirXDefault** <br/> |
| 1  <br/> | Up  <br/> |**visLOJumpDirXUp** <br/> |
| 2  <br/> | Down  <br/> |**visLOJumpDirXDown** <br/> |
   
## <a name="remarks"></a>Remarques

Pour définir l’orientation  horizontale par défaut pour tous les sauts de connecteur sur une page, utilisez la cellule PageLineJumpDirX dans la section Mise en page. 
  
Pour obtenir une référence à la cellule ConLineJumpDirX par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | ConLineJumpDirX  <br/> |
   
Pour obtenir une référence à la cellule ConLineJumpDirX à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowShapeLayout** <br/> |
| Index de la cellule :  <br/> |**visSLOJumpDirX** <br/> |
   

