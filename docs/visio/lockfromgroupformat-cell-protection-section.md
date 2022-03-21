---
title: LockFromGroupFormat, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: abd175af-ad4e-b84a-2687-2c9358653499
ms.openlocfilehash: b51b60f178ef512a477fb89a3c0568471475b741
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63630237"
---
# <a name="lockfromgroupformat-cell-protection-section"></a>LockFromGroupFormat, cellule (section Protection)

Bloque la propagation des modifications de format d’une forme de groupe à ses sous-formes, tout en permettant aux utilisateurs de mettre en forme les sous-formes sélectionnées directement. 
  
La valeur de la cellule LockFromGroupFormat correspond au paramétrage de la case à cocher **Contre la mise en forme de groupe** de la boîte de dialogue **Protection**. 
  
Pour faire référence à la cellule LockFromGroupFormat par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :

 
  
||Valeur |
|:-----|:-----|
|**Nom de cellule :**  <br/> |LockFromGroupFormat  <br/> |
   
Pour faire référence à la cellule LockFromGroupFormat par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :

 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRowLock** <br/> |
|**Index de la cellule :**  <br/> |**visLockFromGroupFormat** <br/> |
   
La valeur par défaut de la cellule est 0 (False).
  

