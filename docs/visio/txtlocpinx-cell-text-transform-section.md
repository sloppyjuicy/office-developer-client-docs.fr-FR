---
title: TxtLocPinX, cellule (section Text Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251275
ms.localizationpriority: medium
ms.assetid: cbfc4e91-10d1-d50e-3e8a-f269f7123276
description: 'Détermine la coordonnée x du centre de rotation du bloc de texte par rapport à l’origine du bloc de texte. La formule par défaut est la suivante :'
ms.openlocfilehash: 04910569b12da5f1a6a7c1e11864d4112f121195
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63626870"
---
# <a name="txtlocpinx-cell-text-transform-section"></a>TxtLocPinX, cellule (section Text Transform)

Détermine la  *coordonnée x*  du centre de rotation du bloc de texte par rapport à l’origine du bloc de texte. La formule par défaut est la suivante : 
  
= TxtWidth \* 0.5
  
Cette formule calcule le centre horizontal du bloc de texte.
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule TxtLocPinX par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de la cellule :**  <br/> | TxtLocPinX  <br/> |
   
Pour obtenir une référence à la cellule TxtLocPinX par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowTextXForm** <br/> |
| **Index de la cellule :**  <br/> |**visXFormLocPinX** <br/> |
   

