---
title: TxtLocPinX, cellule (section Text Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251275
localization_priority: Normal
ms.assetid: cbfc4e91-10d1-d50e-3e8a-f269f7123276
description: 'Détermine le x-coordonnées du centre du bloc de texte de rotation par rapport à l’origine du bloc de texte. La formule par défaut est la suivante :'
ms.openlocfilehash: 6eb48532bb19bce5b0d22ed2cd0997014721df88
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789936"
---
# <a name="txtlocpinx-cell-text-transform-section"></a>TxtLocPinX, cellule (section Text Transform)

Détermine le *x* -coordonnées du centre du bloc de texte de rotation par rapport à l’origine du bloc de texte. La formule par défaut est la suivante : 
  
= TxtWidth \* 0,5
  
Cette formule calcule le centre horizontal du bloc de texte.
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule TxtLocPinX par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | TxtLocPinX  <br/> |
   
Pour obtenir une référence à la cellule TxtLocPinX par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowTextXForm** <br/> |
| Index de la cellule :  <br/> |**visXFormLocPinX** <br/> |
   

