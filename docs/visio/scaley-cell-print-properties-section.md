---
title: ScaleY, cellule (section Print Properties)
description: La cellule ScaleY (section Propriétés d’impression) spécifie le pourcentage d’agrandissement de la page de dessin sur la page de l’imprimante.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033788
ms.localizationpriority: medium
ms.assetid: 02835aff-455b-ffeb-d53b-28387b6ce361
ms.openlocfilehash: 9208f7063426831244fec3fad4ae082e7edca988
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65854622"
---
# <a name="scaley-cell-print-properties-section"></a>ScaleY, cellule (section Print Properties)

Spécifie le pourcentage d’agrandissement de la page de dessin sur la page d’imprimante.
  
## <a name="remarks"></a>Remarques

Cette valeur n’est utilisée que lorsque la valeur de la cellule OnPage est FALSE. Les cellules ScaleX et ScaleY ont toujours la même valeur, qui correspond à la valeur de l’onglet **Ajuster au** paramètre de l’onglet **Installation** de l’impression dans la boîte de dialogue **Mise** en page (sous l’onglet **Création** , cliquez sur la flèche **Mise** en page). 
  
Pour obtenir une référence à la cellule ScaleY par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de la cellule :**  <br/> |Scaley  <br/> |
   
Pour obtenir une référence à la cellule ScaleY à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRowPrintProperties** <br/> |
|**Index de la cellule :**  <br/> |**visPrintPropertiesScaleY** <br/> |
   

