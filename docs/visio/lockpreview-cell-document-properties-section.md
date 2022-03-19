---
title: LockPreview, cellule (section Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251742
ms.localizationpriority: medium
ms.assetid: 5a2bb1a7-e688-d32f-f231-ac6916d838a6
description: Détermine si un aperçu est enregistré chaque fois que vous enregistrez un dessin.
ms.openlocfilehash: 1e1f77fa8dfd2a86887992a372a0c86f741926c2
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63629376"
---
# <a name="lockpreview-cell-document-properties-section"></a>LockPreview, cellule (section Document Properties)

Détermine si un aperçu est enregistré chaque fois que vous enregistrez un dessin.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | Un aperçu n'est pas enregistré chaque fois que vous enregistrez un dessin. |
| FALSE  <br/> | Un aperçu est enregistré chaque fois que vous enregistrez un dessin. |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule LockPreview par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de la cellule :**  <br/> | LockPreview  <br/> |
   
Pour obtenir une référence à la cellule LockPreview à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowDoc** <br/> |
| **Index de la cellule :**  <br/> |**visDocLockPreview** <br/> |
   

