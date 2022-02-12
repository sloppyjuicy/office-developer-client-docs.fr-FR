---
title: LockReplace Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: b3880511-dd27-4dc2-9e50-a49084ef8195
description: Indique si une forme peut participer à une opération de remplacement (en tant que cible ou forme de remplacement).
ms.openlocfilehash: e672b57e440973126463a8e21b0e73a98ac564bd
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62778348"
---
# <a name="lockreplace-cell-protection-section"></a>LockReplace Cell (Protection Section)

Indique si une forme peut participer à une opération de remplacement (en tant que cible ou forme de remplacement). 
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |La forme ne peut pas être remplacée ou utilisée comme forme de remplacement. Pour une forme sur la zone de dessin **, le bouton** Modifier la forme est désactivé lorsque la forme est sélectionnée. Pour une forme sur un gabarit, la forme n’apparaît pas en tant que forme de  remplacement lorsque l’utilisateur clique sur le bouton Modifier la forme. |
|FALSE  <br/> |La forme peut être remplacée ou utilisée comme forme de remplacement. |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **LockReplace** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | LockReplace  <br/> |
   
Pour obtenir une référence à la **cellule LockReplace** à l’aide d’un index à partir d’un programme, utilisez la **propriété CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowLock** <br/> |
| Index de la cellule :  <br/> |**visLockReplace** <br/> |
   

