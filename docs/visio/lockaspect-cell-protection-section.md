---
title: LockAspect, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251218
ms.localizationpriority: medium
ms.assetid: e9bfced5-af29-f86c-8604-44ec9a573229
description: Verrouille le rapport hauteur/largeur de la forme afin que cette dernière puisse être dimensionnée uniquement de façon proportionnelle, ce qui signifie qu’il est impossible de modifier une seule cote à la fois.
ms.openlocfilehash: ee7ca3df9cce5f11a83fb8665d9db93d21f3c27e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628019"
---
# <a name="lockaspect-cell-protection-section"></a>LockAspect, cellule (section Protection)

Verrouille le rapport hauteur/largeur de la forme afin que cette dernière puisse être dimensionnée uniquement de façon proportionnelle, ce qui signifie qu’il est impossible de modifier une seule cote à la fois.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | Le rapport hauteur/largeur est verrouillé.  <br/> |
| FALSE  <br/> | Le rapport hauteur/largeur n'est pas verrouillé.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule LockAspect par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | LockAspect  <br/> |
   
Pour obtenir une référence à la cellule LockAspect à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowLock** <br/> |
| Index de la cellule :  <br/> |**visLockAspect** <br/> |
   

