---
title: Calendar, cellule (section Custom Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60027
ms.localizationpriority: medium
ms.assetid: f5dcc6d9-474a-9ecb-21f5-56415d934890
description: Détermine le calendrier utilisé pour les données de forme lorsque le type de données est Date.
ms.openlocfilehash: 21abee2b1b11057e8140e4d64e5e35a019aef1e9
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62777284"
---
# <a name="calendar-cell-shape-data-section"></a>Calendar, cellule (section Custom Properties)

Détermine le calendrier utilisé pour les données de forme lorsque le type de données est Date.
  
## <a name="remarks"></a>Remarques

Les valeurs possibles sont : 0 (Occidental), 1 (Hijri arabe), 2 (Lunaire hébraïque), 3 (Calendrier taïwanais), 4 (Calendrier impérial japonais), 5 (Bouddhiste Thaï), 6 (Danki coréen), 7 (Hindou ère Saka), 8 (Transcription anglaise) et 9 (Transcription française). 
  
Pour obtenir une référence à la cellule Calendar par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Prop.  *nom*  . Calendrier où Prop.  *nom est*  le nom de ligne  <br/> |
   
Pour obtenir une référence à la cellule Calendar à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionProp** <br/> |
| Index de la ligne :  <br/> |**visRowProp** +   *i* où *i* = 0, 1, 2... |
| Index de la cellule :  <br/> |**visCustPropsCalendar** <br/> |
   

