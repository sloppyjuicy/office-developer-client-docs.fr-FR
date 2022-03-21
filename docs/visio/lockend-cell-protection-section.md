---
title: LockEnd, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm620
ms.localizationpriority: medium
ms.assetid: e9742142-4d34-1ba9-480e-d1ecff4fc7cd
description: Verrouille le point de fin (EndX, EndY) d'une forme 1D à un emplacement donné.
ms.openlocfilehash: 605a670ee1eb7f2e8fb90cc96d3caaa448e032a1
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63629404"
---
# <a name="lockend-cell-protection-section"></a>LockEnd, cellule (section Protection)

Verrouille le point de fin (EndX, EndY) d'une forme 1D à un emplacement donné.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | Le point de fin est verrouillé. |
| FALSE  <br/> | Le point de fin n'est pas verrouillé. |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule LockEnd par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de la cellule :**  <br/> | LockEnd  <br/> |
   
Pour obtenir une référence à la cellule LockEnd à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowLock** <br/> |
| **Index de la cellule :**  <br/> |**visLockEnd** <br/> |
   

