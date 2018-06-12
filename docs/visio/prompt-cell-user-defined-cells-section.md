---
title: Prompt, cellule (section User-Defined Cells)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm840
localization_priority: Normal
ms.assetid: d0f91e7d-2373-cfef-e105-fb17e77c7f2d
description: Indique un message descriptif ou commentaire pour la cellule définie par l'utilisateur. L’application insère automatiquement le texte d’invite les guillemets doubles () pour indiquer qu’il s’agit d’une chaîne de texte. Si vous tapez un signe égal (=) et omettez les guillemets, vous pouvez entrer une formule dans une cellule qui évalue l’application.
ms.openlocfilehash: a7f8757af3e324a89f49bf5d19185b7a22173ff5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789372"
---
# <a name="prompt-cell-user-defined-cells-section"></a>Prompt, cellule (section User-Defined Cells)

Contient un message descriptif ou commentaire associé à la cellule définie par l'utilisateur. L'application encadre automatiquement le message par des guillemets (" ") pour signaler qu'il s'agit d'une chaîne de texte. Si vous tapez un signe égal (=) sans guillemets, vous pouvez entrer dans cette cellule une formule qui est alors évaluée par l'application.
  
## <a name="remarks"></a>Note

Pour obtenir une référence à la cellule Prompt par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Utilisateur.  *Nom* . Où invite utilisateur.  *Name* est le nom de ligne  <br/> |
   
Pour obtenir une référence à la cellule Prompt par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionUser** <br/> |
| Index de la ligne :  <br/> |**visRowUser +** *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visUserPrompt** <br/> |
   

