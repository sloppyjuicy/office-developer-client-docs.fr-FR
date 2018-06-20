---
title: TxtPinY, cellule (section Text Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1045
localization_priority: Normal
ms.assetid: 88ddf4b5-8248-8c1a-c387-09a607639d26
description: 'Détermine la valeur y-coordonnées du centre du bloc de texte de rotation par rapport à l’origine de la forme. La formule par défaut est la suivante :'
ms.openlocfilehash: e8101463413b177bf8ddd80ed52964d3eeae788f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789953"
---
# <a name="txtpiny-cell-text-transform-section"></a>TxtPinY, cellule (section Text Transform)

Détermine la valeur *y* -coordonnées du centre du bloc de texte de rotation par rapport à l’origine de la forme. La formule par défaut est la suivante : 
  
= Hauteur \* 0,5
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule TxtPinY par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | TxtPinY  <br/> |
   
Pour obtenir une référence à la cellule TxtPinY par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowTextXForm** <br/> |
| Index de la cellule :  <br/> |**visXFormPinY** <br/> |
   

