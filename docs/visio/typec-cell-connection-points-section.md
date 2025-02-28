---
title: Type / C, cellule (section Connection Points)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251723
ms.localizationpriority: medium
ms.assetid: 2264d026-2041-3855-2b23-553ce67ae69d
description: Définit le type du point de connexion.
ms.openlocfilehash: 8591a1f7b0a601d2acc2e6d8417ba70b8eedb8f8
ms.sourcegitcommit: b2c5a02b2d0abd2da2542089fc3f83ff07e121e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2022
ms.locfileid: "63507947"
---
# <a name="type--c-cell-connection-points-section"></a>Type / C, cellule (section Connection Points)

Définit le type du point de connexion.
  
|**Valeur**|**Type**|**Constante d'automation**|
|:-----|:-----|:-----|
|0  <br/> |Vers l’intérieur  <br/> |**visCnnctTypeInward** <br/> |
|1  <br/> |Vers l’extérieur  <br/> |**visCnnctTypeOutward** <br/> |
|2  <br/> |Vers l’intérieur vers l’extérieur &amp;  <br/> |**visCnnctTypeInwardOutward** <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir le type du point de connexion en choisissant l’outil **Lien**, en sélectionnant une forme et en cliquant avec le bouton droit de la souris sur un point de connexion. Dans ce cas, vous devez utiliser le mode [développeur](run-in-developer-mode-display-the-developer-tab.md). 
  
Pour obtenir une référence à la cellule Type / C par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de cellule :**  <br/> |Connections.Type[  *i*  ] where  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule Type / C par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionConnectionPts** <br/> |
|**Index de la ligne :**  <br/> |**visRowConnectionPts** +   *i* où *i* = 0, 1, 2... |
|**Index de la cellule :**  <br/> |**visCnnctType** (lignes non étendues) **visCnnctC** (lignes étendues)  <br/> |
   
Pour plus d'informations sur les lignes non étendues et étendues, reportez-vous à la ligne Connection Points.
  

