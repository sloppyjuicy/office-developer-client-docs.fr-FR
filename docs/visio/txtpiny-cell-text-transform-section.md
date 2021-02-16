---
title: TxtPinY, cellule (section Text Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1045
localization_priority: Normal
ms.assetid: 88ddf4b5-8248-8c1a-c387-09a607639d26
description: 'Détermine la coordonnée y du centre de rotation du bloc de texte par rapport à l’origine de la forme. La formule par défaut est la suivante :'
ms.openlocfilehash: fc62ac76aa24a698d956690df6e5d1e7cff3fb5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418490"
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
   

