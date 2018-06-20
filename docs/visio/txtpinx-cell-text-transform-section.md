---
title: TxtPinX, cellule (section Text Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1040
localization_priority: Normal
ms.assetid: d0c0fe52-6a9e-e40e-394e-83a851db55a4
description: 'Détermine le x-coordonnées du centre du bloc de texte de rotation par rapport à l’origine de la forme. La formule par défaut est la suivante :'
ms.openlocfilehash: df103557d103dbde7e4a1c8d67cabe37a0af9311
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789947"
---
# <a name="txtpinx-cell-text-transform-section"></a>TxtPinX, cellule (section Text Transform)

Détermine le *x* -coordonnées du centre du bloc de texte de rotation par rapport à l’origine de la forme. La formule par défaut est la suivante : 
  
= Largeur \* 0,5
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule TxtPinX par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | TxtPinX  <br/> |
   
Pour obtenir une référence à la cellule TxtPinX par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowTextXForm** <br/> |
| Index de la cellule :  <br/> |**visXFormPinX** <br/> |
   

