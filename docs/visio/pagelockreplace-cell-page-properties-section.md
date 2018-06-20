---
title: PageLockReplace, cellule (Section Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59c36555-42af-4729-aea7-0332d1da6e3b
description: Indique si le bouton Remplacer la forme doit être désactivé pour cette page.
ms.openlocfilehash: b3956b3e2f2fcd5c4f82089e08a6e32200374778
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789210"
---
# <a name="pagelockreplace-cell-page-properties-section"></a>PageLockReplace, cellule (Section Page Properties)

Indique si le bouton **Remplacer la forme** doit être désactivé pour cette page. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Le bouton **Modifier la forme** est grisé lorsque cette page est active.  <br/> |
|FALSE  <br/> |Le bouton **Modifier la forme** n’est pas désactivé par cette page. Le bouton peut-être toujours être grisé if : le **DocLockReplace** sur la **propriété DocumentSheet** est définie sur **TRUE**; la cellule **LockReplace** de la forme sélectionnée est définie sur **TRUE**.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **PageLockReplace** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | PageLockReplace  <br/> |
   
Pour obtenir une référence à la cellule **PageLockReplace** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowPage** <br/> |
| Index de la cellule :  <br/> |**visPageLockReplace** <br/> |
   

