---
title: TxtLocPinX, cellule (section Text Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251275
localization_priority: Normal
ms.assetid: cbfc4e91-10d1-d50e-3e8a-f269f7123276
description: "Détermine la coordonnée x du centre de rotation du bloc de texte par rapport à l'origine du bloc de texte. La formule par défaut est la suivante :"
ms.openlocfilehash: 390f8129e8000a043969eda0ab1c8e4ef62515ef
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425854"
---
# <a name="txtlocpinx-cell-text-transform-section"></a>TxtLocPinX, cellule (section Text Transform)

Détermine la coordonnée *x* du centre de rotation du bloc de texte par rapport à l'origine du bloc de texte. La formule par défaut est la suivante : 
  
= TxtWidth \* 0,5
  
Cette formule calcule le centre horizontal du bloc de texte.
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule TxtLocPinX par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | TxtLocPinX  <br/> |
   
Pour obtenir une référence à la cellule TxtLocPinX par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowTextXForm** <br/> |
| Index de la cellule :  <br/> |**visXFormLocPinX** <br/> |
   

