---
title: PageLockReplace Cell (Page Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59c36555-42af-4729-aea7-0332d1da6e3b
description: Indique si le bouton remplacer la forme doit être désactivé pour cette page.
ms.openlocfilehash: c0495d47a81ed7a23e758c531f7d754291c47852
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433100"
---
# <a name="pagelockreplace-cell-page-properties-section"></a>PageLockReplace Cell (Page Properties Section)

Indique si le bouton **remplacer la forme** doit être désactivé pour cette page. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Le bouton **modifier la forme** est grisé lorsque cette page est active.  <br/> |
|FALSE  <br/> |Le bouton **modifier la forme** n'est pas désactivé par cette page. Le bouton peut toujours être grisé si: le **DocLockReplace** sur le **DocumentSheet** est défini sur **true**; la cellule **LockReplace** de la forme sélectionnée est définie sur **true**.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **PageLockReplace** par un nom à partir d'une autre formule, par valeur de l'attribut **N** d'un élément de **cellule** ou d'un programme en faisant appel à la propriété **CellsU** , utilisez: 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | PageLockReplace  <br/> |
   
Pour obtenir une référence à la cellule **PageLockReplace** à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants: 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowPage** <br/> |
| Index de la cellule :  <br/> |**visPageLockReplace** <br/> |
   

