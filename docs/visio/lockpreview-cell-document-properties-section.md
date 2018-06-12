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
ms.openlocfilehash: 2ef5ea12669a7a6a2b37d599afd24635f7509ac2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789011"
---
# <a name="lockpreview-cell-document-properties-section"></a>LockPreview, cellule (section Document Properties)

Détermine si un aperçu est enregistré chaque fois que vous enregistrez un dessin.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | Un aperçu n'est pas enregistré chaque fois que vous enregistrez un dessin.  <br/> |
| FALSE  <br/> | Un aperçu est enregistré chaque fois que vous enregistrez un dessin.  <br/> |
   
## <a name="remarks"></a>Note

Pour obtenir une référence à la cellule LockPreview par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | LockPreview  <br/> |
   
Pour obtenir une référence à la cellule LockPreview par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowDoc** <br/> |
| Index de la cellule :  <br/> |**visDocLockPreview** <br/> |
   

