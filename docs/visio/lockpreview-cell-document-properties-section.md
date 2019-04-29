---
title: LockPreview, cellule (section Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251742
localization_priority: Normal
ms.assetid: 5a2bb1a7-e688-d32f-f231-ac6916d838a6
description: Détermine si un aperçu est enregistré chaque fois que vous enregistrez un dessin.
ms.openlocfilehash: 91362d8a88cf6db2f4807c655a6d071ebbc731f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418861"
---
# <a name="lockpreview-cell-document-properties-section"></a>LockPreview, cellule (section Document Properties)

Détermine si un aperçu est enregistré chaque fois que vous enregistrez un dessin.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | Un aperçu n'est pas enregistré chaque fois que vous enregistrez un dessin.  <br/> |
| FALSE  <br/> | Un aperçu est enregistré chaque fois que vous enregistrez un dessin.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule LockPreview par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | LockPreview  <br/> |
   
Pour obtenir une référence à la cellule LockPreview à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowDoc** <br/> |
| Index de la cellule :  <br/> |**visDocLockPreview** <br/> |
   

