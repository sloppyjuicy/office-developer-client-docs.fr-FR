---
title: PageLockReplace Cell (Page Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 59c36555-42af-4729-aea7-0332d1da6e3b
description: Indique si le bouton Remplacer la forme doit être désactivé pour cette page.
ms.openlocfilehash: 1ee717d0cd23836788c34659675398248fd76c86
ms.sourcegitcommit: eb9453e5664b01759b602cb5a4cef5b4885128f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2022
ms.locfileid: "63783139"
---
# <a name="pagelockreplace-cell-page-properties-section"></a>PageLockReplace Cell (Page Properties Section)

Indique si le **bouton Remplacer la** forme doit être désactivé pour cette page. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Le **bouton Modifier la** forme est grisé lorsque cette page est active. |
|FALSE  <br/> |Le **bouton Modifier la** forme n’est pas désactivé par cette page. Le bouton peut toujours être grisé si : le **DocLockReplace** de la feuille de **document est définie** sur **TRUE** ; La **cellule LockReplace** de la forme sélectionnée est définie sur **TRUE**. |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **PageLockReplace** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | PageLockReplace  <br/> |
   
Pour obtenir une référence à la **cellule PageLockReplace** à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowPage** <br/> |
| **Index de la cellule :**  <br/> |**visPageLockReplace** <br/> |
   

