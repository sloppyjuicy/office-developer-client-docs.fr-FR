---
title: TxtLocPinY, cellule (section Text Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251276
localization_priority: Normal
ms.assetid: 3f46cfcf-7eac-4a37-e782-39f4e7f8fc43
description: 'Détermine la valeur y-coordonnées du centre du bloc de texte de rotation par rapport à l’origine du bloc de texte. La formule par défaut est la suivante :'
ms.openlocfilehash: 7d43f63b8560df5fc5daf09a429ce30ec976d131
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789945"
---
# <a name="txtlocpiny-cell-text-transform-section"></a>TxtLocPinY, cellule (section Text Transform)

Détermine la valeur *y* -coordonnées du centre du bloc de texte de rotation par rapport à l’origine du bloc de texte. La formule par défaut est la suivante : 
  
= TxtHeight \* 0,5
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule TxtLocPinY par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | TxtLocPinY  <br/> |
   
Pour obtenir une référence à la cellule TxtLocPinY par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowTextXForm** <br/> |
| Index de la cellule :  <br/> |**visXFormLocPinY** <br/> |
   

