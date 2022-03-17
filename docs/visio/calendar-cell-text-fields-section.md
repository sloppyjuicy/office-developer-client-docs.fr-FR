---
title: Calendar, cellule (section Text Fields)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60029
ms.localizationpriority: medium
ms.assetid: 0c3e275e-25f0-3681-03f4-257145c19690
description: Détermine le calendrier utilisé pour un champ de texte lorsque le type de données est Date.
ms.openlocfilehash: 5adc4da32357bb853515ba9a6fbc3c60c53d2e31
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63519852"
---
# <a name="calendar-cell-text-fields-section"></a>Calendar, cellule (section Text Fields)

Détermine le calendrier utilisé pour un champ de texte lorsque le type de données est Date.
  
## <a name="remarks"></a>Remarques

Les valeurs possibles sont : 0 (Occidental), 1 (Hijri arabe), 2 (Lunaire hébraïque), 3 (Calendrier taïwanais), 4 (Calendrier impérial japonais), 5 (Bouddhiste Thaï), 6 (Danki coréen), 7 (Hindou ère Saka), 8 (Transcription anglaise) et 9 (Transcription française). 
  
Pour obtenir une référence à la cellule Calendar par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | Fields.Calendar[  *i*  ] where  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule Calendar à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionTextField** <br/> |
| **Index de la ligne :**  <br/> |**visRowField** +   *i* où *i* = 0, 1, 2... |
| **Index de la cellule :**  <br/> |**visFieldCalendar** <br/> |
   

