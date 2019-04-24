---
title: Type / C, cellule (section Connection Points)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251723
localization_priority: Normal
ms.assetid: 2264d026-2041-3855-2b23-553ce67ae69d
description: Définit le type du point de connexion.
ms.openlocfilehash: a73554d9f3a3bce6a039689d2c0b192a1c5b69aa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359583"
---
# <a name="type--c-cell-connection-points-section"></a>Type / C, cellule (section Connection Points)

Définit le type du point de connexion.
  
|**Valeur**|**Type**|**Constante d'automation**|
|:-----|:-----|:-----|
|0  <br/> |Cadre  <br/> |**visCnnctTypeInward** <br/> |
|0,1  <br/> |Fats  <br/> |**visCnnctTypeOutward** <br/> |
|n°2  <br/> |Vers &amp; l'intérieur  <br/> |**visCnnctTypeInwardOutward** <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir le type du point de connexion en choisissant l’outil **Lien**, en sélectionnant une forme et en cliquant avec le bouton droit de la souris sur un point de connexion. Dans ce cas, vous devez utiliser le mode [développeur](run-in-developer-mode-display-the-developer-tab.md). 
  
Pour obtenir une référence à la cellule Type / C par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |Connections. type [ *i* ] où *i* = <1>, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule Type / C par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionConnectionPts** <br/> |
|Index de la ligne :  <br/> |**visRowConnectionPts** +  *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visCnnctType** (lignes non étendues) **visCnnctC** (lignes étendues)  <br/> |
   
Pour plus d'informations sur les lignes non étendues et étendues, reportez-vous à la ligne Connection Points.
  

