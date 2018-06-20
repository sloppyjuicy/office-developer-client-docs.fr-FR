---
title: Label, cellule (section Shape Data)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm510
localization_priority: Normal
ms.assetid: 6d328b1c-8d92-eb1a-7317-7dd85c674ff9
description: Indique l’intitulé qui s’affiche dans la fenêtre données de forme. Une étiquette est constituée de caractères alphanumériques, y compris le caractère de soulignement (_).
ms.openlocfilehash: 087bcb87a9e47131e6dbcd2d8df5c5da8a06894b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788880"
---
# <a name="label-cell-shape-data-section"></a>Label, cellule (section Shape Data)

Indique l’intitulé qui s’affiche dans la fenêtre **Données de forme** . Une étiquette est constituée de caractères alphanumériques, y compris le caractère de soulignement (_). 
  
## <a name="remarks"></a>Remarques

L’application insère automatiquement la chaîne d’étiquette entre des guillemets dans la cellule, mais les guillemets ne sont pas affichées dans la fenêtre **Données de forme** . 
  
Si aucun texte de l’étiquette n’est trouvé, Visio affiche le nom de la ligne (Prop.Row) dans la fenêtre **Données de forme** . 
  
Pour obtenir une référence à la cellule Label par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |Propriétés. *Nom* . Étiquette où de propriétés.  *Name* est le nom de ligne  <br/> |
   
Pour obtenir une référence à la cellule Label par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionProp** <br/> |
|Index de la ligne :  <br/> |**visRowProp** +  *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visCustPropsLabel** <br/> |
   

