---
title: LockFromGroupFormat, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: abd175af-ad4e-b84a-2687-2c9358653499
ms.openlocfilehash: ef4cd97298108f64f4fdc7fcd5d690bfeeb16bbc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554445"
---
# <a name="lockfromgroupformat-cell-protection-section"></a>LockFromGroupFormat, cellule (section Protection)

Bloque la propagation des modifications de format d’une forme de groupe à ses sous-formes, tout en permettant aux utilisateurs de mettre en forme les sous-formes sélectionnées directement. 
  
La valeur de la cellule LockFromGroupFormat correspond au paramétrage de la case à cocher **Contre la mise en forme de groupe** de la boîte de dialogue **Protection**. 
  
Pour faire référence à la cellule LockFromGroupFormat par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :

 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |LockFromGroupFormat  <br/> |
   
Pour faire référence à la cellule LockFromGroupFormat par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowLock** <br/> |
|Index de la cellule :  <br/> |**visLockFromGroupFormat** <br/> |
   
La valeur par défaut de la cellule est 0 (False).
  

