---
title: DisplayMode, cellule (section Group Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251623
ms.localizationpriority: medium
ms.assetid: e6d72529-aa03-e94b-130c-79ed04336299
description: Détermine le mode d'affichage de la forme de groupe et de ses membres.
ms.openlocfilehash: 22989d22d0e8792e609027662750c4e9f9da73fa
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590337"
---
# <a name="displaymode-cell-group-properties-section"></a>DisplayMode, cellule (section Group Properties)

Détermine le mode d'affichage de la forme de groupe et de ses membres.
  
|**Valeur**|**Mode d’affichage**|**Constante d'automation**|
|:-----|:-----|:-----|
|0  <br/> |Masque la forme de groupe et le texte  <br/> |**visGrpDispModeNone** <br/> |
|1  <br/> |Affiche la forme de groupe derrière ses membres  <br/> |**visGrpDispModeBack** <br/> |
|2  <br/> |Affiche la forme de groupe devant ses membres  <br/> |**visGrpDispModeFront** <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir cette valeur en  sélectionnant  le groupe, [](run-in-developer-mode-display-the-developer-tab.md) en cliquant sur Comportement dans le groupe Création de forme sous l’onglet Développeur, puis en sélectionnant un mode d’affichage dans la liste de données **de** groupe. 
  
Pour obtenir une référence à la cellule DisplayMode par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |DisplayMode  <br/> |
   
Pour obtenir une référence à la cellule DisplayMode à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowGroup** <br/> |
|Index de la cellule :  <br/> |**visGroupDisplayMode** <br/> |
   

