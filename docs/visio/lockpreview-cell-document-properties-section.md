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
ms.openlocfilehash: 022145e20a2749e2e5dea83ebed2bc16c0be8e06
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62771257"
---
# <a name="lockpreview-cell-document-properties-section"></a>LockPreview, cellule (section Document Properties)

Détermine si un aperçu est enregistré chaque fois que vous enregistrez un dessin.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | Un aperçu n'est pas enregistré chaque fois que vous enregistrez un dessin. |
| FALSE  <br/> | Un aperçu est enregistré chaque fois que vous enregistrez un dessin. |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule LockPreview par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | LockPreview  <br/> |
   
Pour obtenir une référence à la cellule LockPreview à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowDoc** <br/> |
| Index de la cellule :  <br/> |**visDocLockPreview** <br/> |
   

