---
title: Prompt, cellule (section User-Defined Cells)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm840
ms.localizationpriority: medium
ms.assetid: d0f91e7d-2373-cfef-e105-fb17e77c7f2d
description: Contient un message descriptif ou commentaire associé à la cellule définie par l'utilisateur. L’application place automatiquement le texte de l’invite entre guillemets () pour indiquer qu’il s’agit d’une chaîne de texte. Si vous tapez un signe égal (=) sans guillemets, vous pouvez entrer dans cette cellule une formule qui est alors évaluée par l'application.
ms.openlocfilehash: 158925e01f710053998189367a9182b2b3eda4b0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623179"
---
# <a name="prompt-cell-user-defined-cells-section"></a>Prompt, cellule (section User-Defined Cells)

Contient un message descriptif ou commentaire associé à la cellule définie par l'utilisateur. L'application encadre automatiquement le message par des guillemets (" ") pour signaler qu'il s'agit d'une chaîne de texte. Si vous tapez un signe égal (=) sans guillemets, vous pouvez entrer dans cette cellule une formule qui est alors évaluée par l'application.
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Prompt par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Utilisateur.  *Nom*  . Invite où User.  *Le nom*  est le nom de la ligne  <br/> |
   
Pour obtenir une référence à la cellule Prompt à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionUser** <br/> |
| Index de la ligne :  <br/> |**visRowUser +** *i*            où  *i*  = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visUserPrompt** <br/> |
   

