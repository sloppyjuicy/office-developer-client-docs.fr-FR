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
ms.openlocfilehash: 019ebd40029c2c07c534a65e81f74bfaca91ac7a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559394"
---
# <a name="txtlocpinx-cell-text-transform-section"></a>TxtLocPinX, cellule (section Text Transform)

Détermine la  *coordonnée x*  du centre de rotation du bloc de texte par rapport à l’origine du bloc de texte. La formule par défaut est la suivante : 
  
= TxtWidth \* 0.5
  
Cette formule calcule le centre horizontal du bloc de texte.
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule TxtLocPinX par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | TxtLocPinX  <br/> |
   
Pour obtenir une référence à la cellule TxtLocPinX par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowTextXForm** <br/> |
| Index de la cellule :  <br/> |**visXFormLocPinX** <br/> |
   

