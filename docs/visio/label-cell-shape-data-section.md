---
title: Label, cellule (section Shape Data)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm510
ms.localizationpriority: medium
ms.assetid: 6d328b1c-8d92-eb1a-7317-7dd85c674ff9
description: Indique l’intitulé que les utilisateurs voient s’afficher dans la fenêtre  Données de forme. Un intitulé se compose de caractères alphanumériques dont le caractère de soulignement (_).
ms.openlocfilehash: 352e113e685a4952f31334947f81d16b0358f375
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618720"
---
# <a name="label-cell-shape-data-section"></a>Label, cellule (section Shape Data)

Indique l’intitulé que les utilisateurs voient s’afficher dans la fenêtre  **Données de forme**. Un intitulé se compose de caractères alphanumériques dont le caractère de soulignement (_). 
  
## <a name="remarks"></a>Remarques

Cet intitulé est automatiquement affiché entre guillemets dans la cellule. Ces guillemets n’apparaissent pas dans la fenêtre **Données de forme**. 
  
Si aucun texte d’intitulé n’est trouvé, Visio affiche le nom de la ligne (Prop.Row) dans la fenêtre **Données de forme**. 
  
Pour obtenir une référence à la cellule Label par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |Prop. *Nom*  . Étiquette où Prop.  *Le nom*  est le nom de la ligne  <br/> |
   
Pour obtenir une référence à la cellule Label à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionProp** <br/> |
|Index de la ligne :  <br/> |**visRowProp**  +   *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visCustPropsLabel** <br/> |
   

