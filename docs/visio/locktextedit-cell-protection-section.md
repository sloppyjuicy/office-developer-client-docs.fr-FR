---
title: LockTextEdit, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm665
localization_priority: Normal
ms.assetid: d8de5fa4-826b-e869-4d9f-997361d05fd8
description: Verrouille le texte d’une forme afin d’empêcher sa modification.
ms.openlocfilehash: f6e5176e3ab654b76c0641b8f642abcf6b1050dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404497"
---
# <a name="locktextedit-cell-protection-section"></a>LockTextEdit, cellule (section Protection)

Verrouille le texte d’une forme afin d’empêcher sa modification.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Le texte ne peut pas être modifié.  <br/> |
| FALSE  <br/> | Le texte peut être modifié.  <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez mettre le texte en forme en appliquant un style à l’aide de la boîte de dialogue **Texte** (sous l’onglet **Accueil**, cliquez sur la flèche **Police**). 
  
Pour obtenir une référence à la cellule LockTextEdit par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | LockTextEdit  <br/> |
   
Pour obtenir une référence à la cellule LockTextEdit à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowLock** <br/> |
| Index de la cellule :  <br/> |**visLockTextEdit** <br/> |
   

