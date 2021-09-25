---
title: LockReplace Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: b3880511-dd27-4dc2-9e50-a49084ef8195
description: Indique si une forme peut participer à une opération de remplacement (en tant que cible ou forme de remplacement).
ms.openlocfilehash: e5220d0d9031aaa383a5dadd4c0c4049ec427eb0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573963"
---
# <a name="lockreplace-cell-protection-section"></a>LockReplace Cell (Protection Section)

Indique si une forme peut participer à une opération de remplacement (en tant que cible ou forme de remplacement). 
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |La forme ne peut pas être remplacée ou utilisée comme forme de remplacement.  <br/> Pour une forme sur la zone de dessin, **le** bouton Modifier la forme est désactivé lorsque la forme est sélectionnée.  <br/> Pour une forme sur un gabarit, la forme n’apparaît pas en tant que forme de remplacement lorsque l’utilisateur clique sur le bouton Modifier la forme.   <br/> |
|FALSE  <br/> |La forme peut être remplacée ou utilisée comme forme de remplacement.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **LockReplace** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU,** utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | LockReplace  <br/> |
   
Pour obtenir une référence à la **cellule LockReplace** à l’aide d’un index à partir d’un programme, utilisez la **propriété CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowLock** <br/> |
| Index de la cellule :  <br/> |**visLockReplace** <br/> |
   

