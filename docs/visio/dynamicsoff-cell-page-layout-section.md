---
title: DynamicsOff, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251641
localization_priority: Normal
ms.assetid: 055764aa-9681-ffb0-83ce-fdd612fe37af
description: Détermine si les formes positionnables se déplacent et si les connecteurs sont repositionnés autour des autres formes et des connecteurs sur la page de dessin.
ms.openlocfilehash: d1075ab1b0512d5db1c7b7a5f2895305318dae7d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437475"
---
# <a name="dynamicsoff-cell-page-layout-section"></a>DynamicsOff, cellule (section Page Layout)

Détermine si les formes positionnables se déplacent et si les connecteurs sont repositionnés autour des autres formes et des connecteurs sur la page de dessin.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | Désactive le repositionnement automatique.  <br/> |
| FALSE  <br/> | Active le repositionnement automatique.  <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez désactiver le repositionnement automatique pour augmenter les performances de votre solution. Par exemple, si votre solution ajoute des formes positionnables sur un dessin et si vous ne souhaitez pas que l'application repositionne les connecteurs et les formes chaque fois que vous ajoutez une forme, vous pouvez désactiver cette fonction, puis la réactiver après que votre solution a fini d'ajouter des formes.
  
Pour obtenir une référence à la cellule DynamcOff par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | DynamcOff  <br/> |
   
Pour obtenir une référence à la cellule DynamcOff à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowPageLayout** <br/> |
| Index de la cellule :  <br/> |**visPLODynamicsOff** <br/> |
   

