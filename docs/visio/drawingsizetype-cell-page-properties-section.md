---
title: DrawingSizeType, cellule (section Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm275
localization_priority: Normal
ms.assetid: 7fe270e8-0dff-bf1f-dfc0-c0608af79f59
description: Détermine la taille du dessin.
ms.openlocfilehash: 33c85b6c2f0587654038eaec1a9490ca8bd8301b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351456"
---
# <a name="drawingsizetype-cell-page-properties-section"></a>DrawingSizeType, cellule (section Page Properties)

Détermine la taille du dessin.
  
|**Value**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
|0  <br/> |Identique au papier de l’imprimante  <br/> |**visPrintSetup** <br/> |
|0,1  <br/> |Ajuster la page au contenu du dessin  <br/> |**visTight** <br/> |
|n°2  <br/> |Standard  <br/> |**visStandard** <br/> |
|3  <br/> |Taille de page personnalisée  <br/> |**visCustom** <br/> |
|4  <br/> |Taille de dessin à l’échelle personnalisée  <br/> |**visLogical** <br/> |
|disque  <br/> |Métrique (ISO)  <br/> |**visDSMetric** <br/> |
|6.x  <br/> |Ingénierie ANSI  <br/> |**visDSEngr** <br/> |
|7j/7  <br/> |Architecturale ANSI  <br/> |**visDSArch** <br/> |
   
## <a name="remarks"></a>Remarques

Pour définir la taille du dessin, utilisez la boîte de dialogue **Mise en page** (cliquez sur la flèche **Mise en page** sous l’onglet **Création**) ou redimensionnez manuellement la page à l’aide de la souris. 
  
Pour obtenir une référence à la cellule DrawingSizeType par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |DrawingSizeType  <br/> |
   
Pour obtenir une référence à la cellule DrawingSizeType à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**Définis** <br/> |
|Index de la ligne :  <br/> |**visRowPage** <br/> |
|Index de la cellule :  <br/> |**visPageDrawSizeType** <br/> |
   

