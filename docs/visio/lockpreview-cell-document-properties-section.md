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
ms.openlocfilehash: 48ec2c7f8ae49bae5a8e2bfe2d4534a48a681807
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615871"
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
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowDoc** <br/> |
| Index de la cellule :  <br/> |**visDocLockPreview** <br/> |
   

