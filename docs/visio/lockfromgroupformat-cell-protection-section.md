---
title: LockFromGroupFormat, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: abd175af-ad4e-b84a-2687-2c9358653499
ms.openlocfilehash: 95633ab7a4127564fef65062bcf328d4364ebd86
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19789014"
---
# <a name="lockfromgroupformat-cell-protection-section"></a>LockFromGroupFormat, cellule (section Protection)

Blocs de format des modifications à une forme de groupe soient propagées à ses sous-formes, tout en permettant aux utilisateurs de mettre en forme directement les sous-formes sélectionnées. 
  
La valeur de la cellule LockFromGroupFormat correspond au paramètre **de groupe mise en forme de** case à cocher dans la boîte de dialogue **Protection** . 
  
Pour faire référence à la cellule LockFromGroupFormat par un nom à partir d’une autre formule ou d’un programme, utilisez la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |LockFromGroupFormat  <br/> |
   
Pour faire référence à la cellule LockFromGroupFormat par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowLock** <br/> |
|Index de la cellule :  <br/> |**visLockFromGroupFormat** <br/> |
   
La valeur par défaut de la cellule est 0 (False).
  

