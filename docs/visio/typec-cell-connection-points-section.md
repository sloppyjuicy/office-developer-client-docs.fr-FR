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
ms.openlocfilehash: 12c953a160ab99aad007e9b2bb9089d651aee553
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789954"
---
# <a name="type--c-cell-connection-points-section"></a>Type / C, cellule (section Connection Points)

Définit le type du point de connexion.
  
|**Valeur**|**Type**|**Constante d’Automation**|
|:-----|:-----|:-----|
|0  <br/> |Vers l'intérieur  <br/> |**visCnnctTypeInward** <br/> |
|1  <br/> |Vers l'extérieur  <br/> |**visCnnctTypeOutward** <br/> |
|2  <br/> |Vers l’intérieur &amp; vers l’extérieur  <br/> |**visCnnctTypeInwardOutward** <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir le type de point de connexion en choisissant l’outil **connecteur** , sélectionner une forme, puis cliquez sur un point de connexion. Pour ce faire, vous devez exécuter en mode [développeur](run-in-developer-mode-display-the-developer-tab.md) . 
  
Pour obtenir une référence au Type / C, cellule par un nom à partir d’une autre formule ou d’un programme à l’aide de la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |Connections.Type [ *i* ] où *i* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence au Type / C, cellule par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionConnectionPts** <br/> |
|Index de la ligne :  <br/> |**visRowConnectionPts** +  *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visCnnctType** (lignes non étendues) **visCnnctC** (lignes étendues)  <br/> |
   
Pour plus d'informations sur les lignes non étendues et étendues, reportez-vous à la ligne Connection Points.
  

