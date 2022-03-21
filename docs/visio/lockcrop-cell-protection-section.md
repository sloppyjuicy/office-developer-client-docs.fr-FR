---
title: LockCrop, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm610
ms.localizationpriority: medium
ms.assetid: ae05de63-b527-66e6-2c79-056c9c92ec95
description: Verrouille un objet d'un autre programme afin d'empêcher qu'il ne soit découpé avec l'outil Découpe.
ms.openlocfilehash: ded9d68be202bcfe7c9a28f2a3651e0d5d4ee6b7
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63632391"
---
# <a name="lockcrop-cell-protection-section"></a>LockCrop, cellule (section Protection)

Verrouille un objet d'un autre programme afin d'empêcher qu'il ne soit découpé avec l'outil **Découpe**. 
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | La forme ne peut pas être découpée.  <br/> |
| FALSE  <br/> | La forme peut être découpée. |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule LockCrop par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de la cellule :**  <br/> | LockCrop  <br/> |
   
Pour obtenir une référence à la cellule LockCrop à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowLock** <br/> |
| **Index de la cellule :**  <br/> |**visLockCrop** <br/> |
   

