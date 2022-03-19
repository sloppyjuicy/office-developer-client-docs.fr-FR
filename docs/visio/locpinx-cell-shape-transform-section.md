---
title: LocPinX, cellule (section Shape Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm680
ms.localizationpriority: medium
ms.assetid: b82feade-5793-8a6e-3ff4-69a4cbdd2cf9
description: 'Représente la coordonnée x de l’axe de la forme (centre de rotation) par rapport à l’origine de la forme. La formule par défaut permettant de déterminer LocPinX est la suivante :'
ms.openlocfilehash: e3b41c267a41653f3cbccdf73b33f60a35f4de84
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63634469"
---
# <a name="locpinx-cell-shape-transform-section"></a>LocPinX, cellule (section Shape Transform)

Représente la  *coordonnée x*  de l’axe de la forme (centre de rotation) par rapport à l’origine de la forme. La formule par défaut permettant de déterminer LocPinX est la suivante : 
  
= Largeur \* 0,5
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule LocPinX par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de la cellule :**  <br/> | LocPinX  <br/> |
   
Pour obtenir une référence à la cellule LocPinX à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowXFormOut** <br/> |
| **Index de la cellule :**  <br/> |**visXFormLocPinX** <br/> |
   

