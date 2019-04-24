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
ms.openlocfilehash: f1fc72484d94788ca2798760ca935c89c3e841ad
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342888"
---
# <a name="shdwtype-cell-page-properties-section"></a>ShdwType, cellule (section Page Properties)

Indique le type d'ombre par défaut d'une page.
  
|**Value**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
| 0,1  <br/> | Simple  <br/> |**visFSTSimple** <br/> |
| n°2  <br/> | Italique  <br/> |**visFSTOblique** <br/> |
|3  <br/> |Intérieur  <br/> |**visFSTInner** <br/> |
   
## <a name="remarks"></a>Remarques

 Le type d'ombre décrit dans cette cellule est utilisé chaque fois que la cellule ShapeShdwType (le type d'ombre d'une forme individuelle sur la page) est définie sur page default (**visFSTPageDefault** ). 
  
Les ombres simples sont décrites comme des ombres de décalage dans l'interface utilisateur. Une ombre simple donne l'impression que la forme a son ombre portée sur un plan parallèle situé à une certaine distance derrière elle. Les ombres obliques sont décrites comme telles dans l'interface utilisateur et donnent l'impression d'une ombre portée sur un plan perpendiculaire à la forme. 
  
Pour obtenir une liste des types d’ombre simples et obliques prédéfinis, reportez-vous à la liste **Style** sous l’onglet **Ombres** de la boîte de dialogue **Mise en page** (sous l’onglet **Création**, cliquez sur la flèche **Mise en page**). 
  
Pour obtenir une référence à la cellule ShdwType par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | ShdwType  <br/> |
   
Pour obtenir une référence à la cellule ShdwType par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowPage** <br/> |
| Index de la cellule :  <br/> |**visPageShdwType** <br/> |
   

