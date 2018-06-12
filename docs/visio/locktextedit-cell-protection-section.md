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
ms.openlocfilehash: 7f8800f0b260e808a46ec123d27784f3dd92e847
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789022"
---
# <a name="locktextedit-cell-protection-section"></a>LockTextEdit, cellule (section Protection)

Verrouille le texte d’une forme afin d’empêcher sa modification.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Le texte ne peut pas être modifié.  <br/> |
| FALSE  <br/> | Le texte peut être modifié.  <br/> |
   
## <a name="remarks"></a>Note

Vous pouvez mettre le texte en forme en appliquant un style dans la boîte de dialogue **texte** (sous l’onglet **accueil** , cliquez sur la flèche **police** ). 
  
Pour obtenir une référence à la cellule LockTextEdit par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | LockTextEdit  <br/> |
   
Pour obtenir une référence à la cellule LockTextEdit par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowLock** <br/> |
| Index de la cellule :  <br/> |**visLockTextEdit** <br/> |
   

