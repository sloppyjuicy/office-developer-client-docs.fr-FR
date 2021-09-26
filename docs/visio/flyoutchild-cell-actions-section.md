---
title: FlyoutChild, cellule (section Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80003
ms.localizationpriority: medium
ms.assetid: b2405457-843c-0d46-5f4f-9c413826c3f1
description: Détermine si la ligne est un menu flottant enfant de la dernière ligne se trouvant au-dessus d’elle si cette dernière n’est pas un menu flottant enfant.
ms.openlocfilehash: e5409d16df7b91c855a95e7b9deb2121ec4e63b3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612798"
---
# <a name="flyoutchild-cell-actions-section"></a>FlyoutChild, cellule (section Actions)

Détermine si la ligne est un menu flottant enfant de la dernière ligne se trouvant au-dessus d’elle si cette dernière n’est pas un menu flottant enfant. 
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule FlyoutChild par le nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |Actions. *nom*  . FlyoutChildwhere Actions.  *name*  est le nom de la ligne Actions  <br/> |
   
Pour obtenir une référence à la cellule FlyoutChild à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionAction** <br/> |
|Index de la ligne :  <br/> |**visRowAction**  +   *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visActionFlyoutChild** <br/> |
   

