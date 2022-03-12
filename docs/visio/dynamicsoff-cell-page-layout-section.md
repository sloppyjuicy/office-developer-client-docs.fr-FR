---
title: DynamicsOff, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251641
ms.localizationpriority: medium
ms.assetid: 055764aa-9681-ffb0-83ce-fdd612fe37af
description: Détermine si les formes positionnables se déplacent et si les connecteurs sont repositionnés autour des autres formes et des connecteurs sur la page de dessin.
ms.openlocfilehash: 4975aeed0dd53b9846261b77b43ee620b371491d
ms.sourcegitcommit: 7b410a51d1e8c97e9cce8d4aa75074162b7d9485
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/12/2022
ms.locfileid: "63448621"
---
# <a name="dynamicsoff-cell-page-layout-section"></a>DynamicsOff, cellule (section Page Layout)

Détermine si les formes positionnables se déplacent et si les connecteurs sont repositionnés autour des autres formes et des connecteurs sur la page de dessin.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | Désactive le repositionnement automatique. |
| FALSE  <br/> | Active le repositionnement automatique. |
   
## <a name="remarks"></a>Remarques

Vous pouvez désactiver le repositionnement automatique pour augmenter les performances de votre solution. Par exemple, si votre solution ajoute des formes positionnables sur un dessin et si vous ne souhaitez pas que l'application repositionne les connecteurs et les formes chaque fois que vous ajoutez une forme, vous pouvez désactiver cette fonction, puis la réactiver après que votre solution a fini d'ajouter des formes.
  
Pour obtenir une référence à la cellule DynamcOff par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de la cellule :**  <br/> | DynamicsOff  <br/> |
   
Pour obtenir une référence à la cellule DynamcOff à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowPageLayout** <br/> |
| **Index de la cellule :**  <br/> |**visPLODynamicsOff** <br/> |
   

