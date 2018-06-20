---
title: ShdwType, cellule (section Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60084
localization_priority: Normal
ms.assetid: 551166d0-3aaa-0fd7-e742-cf3450ba90ed
description: Indique le type d'ombre par défaut d'une page.
ms.openlocfilehash: 1fc5c31a723d5d409110d94ff543a45dadabf264
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789713"
---
# <a name="shdwtype-cell-page-properties-section"></a>ShdwType, cellule (section Page Properties)

Indique le type d'ombre par défaut d'une page.
  
|**Valeur**|**Description**|**Constante d’Automation**|
|:-----|:-----|:-----|
| 1  <br/> | Simple  <br/> |**visFSTSimple** <br/> |
| 2  <br/> | Oblique  <br/> |**visFSTOblique** <br/> |
|3  <br/> |Interne  <br/> |**visFSTInner** <br/> |
   
## <a name="remarks"></a>Remarques

 Le type d’ombre décrit dans cette cellule est utilisé chaque fois que la cellule ShapeShdwType (le type d’ombre d’une forme individuelle sur la page) est réglée sur Page Default (**visFSTPageDefault** ). 
  
Types d’ombre simple sont décrits comme des ombres décalage dans l’interface utilisateur (IU). Une ombre simple donne l’effet de la forme de son ombre portée sur un plan parallèle situé certaine distance derrière elle. Ombres obliques sont décrites comme telles dans l’interface utilisateur et donnent l’effet d’une ombre portée sur un plan perpendiculaire à la forme. 
  
Pour une liste des types d’ombre simples et obliques prédéfinis, voir la liste **Style** de l’onglet **ombres** de la boîte de dialogue **Mise en Page** (sous l’onglet **Création** , cliquez sur la flèche **Mise en Page** ). 
  
Pour obtenir une référence à la cellule ShdwType par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | ShdwType  <br/> |
   
Pour obtenir une référence à la cellule ShapeShdwOffsetX par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowPage** <br/> |
| Index de la cellule :  <br/> |**visPageShdwType** <br/> |
   

