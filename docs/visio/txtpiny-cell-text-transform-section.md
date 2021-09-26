---
title: TxtPinY, cellule (section Text Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1045
ms.localizationpriority: medium
ms.assetid: 88ddf4b5-8248-8c1a-c387-09a607639d26
description: 'Détermine la coordonnée y du centre de rotation du bloc de texte par rapport à l’origine de la forme. La formule par défaut est la suivante :'
ms.openlocfilehash: a08e1da3a7e36cf7bfd04d199a949dfe91d6df33
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603234"
---
# <a name="txtpiny-cell-text-transform-section"></a>TxtPinY, cellule (section Text Transform)

Détermine la coordonnée  *y*  du centre de rotation du bloc de texte par rapport à l’origine de la forme. La formule par défaut est la suivante : 
  
= Hauteur \* 0,5
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule TxtPinY par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | TxtPinY  <br/> |
   
Pour obtenir une référence à la cellule TxtPinY par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowTextXForm** <br/> |
| Index de la cellule :  <br/> |**visXFormPinY** <br/> |
   

