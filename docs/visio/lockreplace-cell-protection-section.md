---
title: LockReplace, cellule (Section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b3880511-dd27-4dc2-9e50-a49084ef8195
description: Indique si une forme peut participer à une opération de remplacement (comme une cible ou une forme de remplacement).
ms.openlocfilehash: 6f3e41d6a6c5b28c55e21961de63d0cc20eeb129
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789007"
---
# <a name="lockreplace-cell-protection-section"></a>LockReplace, cellule (Section Protection)

Indique si une forme peut participer à une opération de remplacement (comme une cible ou une forme de remplacement). 
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |La forme ne peut pas être remplacée ou être utilisée comme une forme de remplacement.  <br/> Pour une forme sur la zone de dessin, le bouton **Modifier la forme** est désactivé lorsque la forme est sélectionnée.  <br/> Pour une forme sur un gabarit, la forme n’apparaît pas comme une forme de remplacement lorsque l’utilisateur clique sur le bouton **Modifier la forme** .  <br/> |
|FALSE  <br/> |La forme peut être remplacée ou utilisée comme une forme de remplacement.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **LockReplace** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | LockReplace  <br/> |
   
Pour obtenir une référence à la cellule **LockReplace** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowLock** <br/> |
| Index de la cellule :  <br/> |**visLockReplace** <br/> |
   

