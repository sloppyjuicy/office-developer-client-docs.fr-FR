---
title: ShdwType, cellule (section Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60084
ms.localizationpriority: medium
ms.assetid: 551166d0-3aaa-0fd7-e742-cf3450ba90ed
description: Indique le type d'ombre par défaut d'une page.
ms.openlocfilehash: 0279aaab9e608f482d0f1ecbc24e48012c087b1c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607667"
---
# <a name="shdwtype-cell-page-properties-section"></a>ShdwType, cellule (section Page Properties)

Indique le type d'ombre par défaut d'une page.
  
|**Valeur**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
| 1  <br/> | Simple  <br/> |**visFSTSimple** <br/> |
| 2  <br/> | Oblique  <br/> |**visFSTOblique** <br/> |
|3  <br/> |Interne  <br/> |**visFSTInner** <br/> |
   
## <a name="remarks"></a>Remarques

 Le type d’ombre décrit dans cette cellule est utilisé chaque fois que la cellule ShapeShdwType (le type d’ombre d’une forme individuelle sur la page) est définie sur Page Default (**visFSTPageDefault** ). 
  
Les ombres simples sont décrites comme des ombres de décalage dans l'interface utilisateur. Une ombre simple donne l'impression que la forme a son ombre portée sur un plan parallèle situé à une certaine distance derrière elle. Les ombres obliques sont décrites comme telles dans l'interface utilisateur et donnent l'impression d'une ombre portée sur un plan perpendiculaire à la forme. 
  
Pour obtenir une liste des types d’ombre simples et obliques prédéfinis, reportez-vous à la liste **Style** sous l’onglet **Ombres** de la boîte de dialogue **Mise en page** (sous l’onglet **Création**, cliquez sur la flèche **Mise en page**). 
  
Pour obtenir une référence à la cellule ShdwType par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | ShdwType  <br/> |
   
Pour obtenir une référence à la cellule ShdwType par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowPage** <br/> |
| Index de la cellule :  <br/> |**visPageShdwType** <br/> |
   

