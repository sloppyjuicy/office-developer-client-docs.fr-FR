---
title: LockCrop, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm610
localization_priority: Normal
ms.assetid: ae05de63-b527-66e6-2c79-056c9c92ec95
description: Verrouille un objet à partir d’un autre programme afin d’être découpé avec l’outil découpe.
ms.openlocfilehash: d7f231d5dcb022548477e0817c9d408a8d1b86ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788994"
---
# <a name="lockcrop-cell-protection-section"></a>LockCrop, cellule (section Protection)

Verrouille un objet à partir d’un autre programme afin d’être découpé avec l’outil **découpe** . 
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | La forme ne peut pas être découpée.  <br/> |
| FALSE  <br/> | La forme peut être découpée.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule LockCrop par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | LockCrop  <br/> |
   
Pour obtenir une référence à la cellule LockCrop par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowLock** <br/> |
| Index de la cellule :  <br/> |**visLockCrop** <br/> |
   

