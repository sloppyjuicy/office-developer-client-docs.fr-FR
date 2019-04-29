---
title: LockReplace Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b3880511-dd27-4dc2-9e50-a49084ef8195
description: Indique si une forme peut participer à une opération de remplacement (en tant que forme cible ou de remplacement).
ms.openlocfilehash: 8b0e3175cacd9b906d91a4185dcd98fad604d8bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404140"
---
# <a name="lockreplace-cell-protection-section"></a>LockReplace Cell (Protection Section)

Indique si une forme peut participer à une opération de remplacement (en tant que forme cible ou de remplacement). 
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |La forme ne peut pas être remplacée ou être utilisée comme une forme de remplacement.  <br/> Pour une forme sur la zone de dessin, le bouton **modifier la forme** est désactivé lorsque la forme est sélectionnée.  <br/> Pour une forme dans un gabarit, la forme n'apparaît pas en tant que forme de remplacement lorsque l'utilisateur clique sur le bouton **modifier la forme** .  <br/> |
|FALSE  <br/> |La forme peut être remplacée ou utilisée comme une forme de remplacement.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **LockReplace** par un nom à partir d'une autre formule, par valeur de l'attribut **N** d'un élément de **cellule** ou d'un programme en faisant appel à la propriété **CellsU** , utilisez: 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | LockReplace  <br/> |
   
Pour obtenir une référence à la cellule **LockReplace** à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants: 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowLock** <br/> |
| Index de la cellule :  <br/> |**visLockReplace** <br/> |
   

