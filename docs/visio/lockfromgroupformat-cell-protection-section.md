---
title: LockFromGroupFormat, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: abd175af-ad4e-b84a-2687-2c9358653499
ms.openlocfilehash: 3daeb4704a33ba836cf82c9ab3517c6ca6be8db7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426057"
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
  

