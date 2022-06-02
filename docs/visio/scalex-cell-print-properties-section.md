---
title: ScaleX, cellule (section Print Properties)
description: La cellule ScaleX (section Propriétés d’impression) spécifie le pourcentage d’agrandissement de la page de dessin sur la page de l’imprimante.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60072
ms.localizationpriority: medium
ms.assetid: 5916eadc-37f8-47af-fe54-f6062aea318f
ms.openlocfilehash: fd643737f483613a08314f4e076a1cd3c5ab33fc
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65854664"
---
# <a name="scalex-cell-print-properties-section"></a>ScaleX, cellule (section Print Properties)

Spécifie le pourcentage d’agrandissement de la page de dessin sur la page d’imprimante.
  
## <a name="remarks"></a>Remarques

Cette valeur n’est utilisée que lorsque la valeur de la cellule OnPage est FALSE. Les cellules ScaleX et ScaleY ont toujours la même valeur, qui correspond à la valeur de l’onglet **Ajuster au** paramètre de l’onglet **Installation** de l’impression dans la boîte de dialogue **Mise** en page (sous l’onglet **Création** , cliquez sur la flèche **Mise** en page). 
  
Pour obtenir une référence à la cellule ScaleX par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de la cellule :**  <br/> |Scalex  <br/> |
   
Pour obtenir une référence à la cellule ScaleX à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRowPrintProperties** <br/> |
|**Index de la cellule :**  <br/> |**visPrintPropertiesScaleX** <br/> |
   

