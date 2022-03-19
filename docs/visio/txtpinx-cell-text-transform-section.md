---
title: TxtPinX, cellule (section Text Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1040
ms.localizationpriority: medium
ms.assetid: d0c0fe52-6a9e-e40e-394e-83a851db55a4
description: 'Détermine la coordonnée x du centre de rotation du bloc de texte par rapport à l’origine de la forme. La formule par défaut est la suivante :'
ms.openlocfilehash: 253a058963bba8f55daba67843e2280c08cfcb33
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63626863"
---
# <a name="txtpinx-cell-text-transform-section"></a>TxtPinX, cellule (section Text Transform)

Détermine la  *coordonnée x*  du centre de rotation du bloc de texte par rapport à l’origine de la forme. La formule par défaut est la suivante : 
  
= Largeur \* 0,5
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule TxtPinX par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de la cellule :**  <br/> | TxtPinX  <br/> |
   
Pour obtenir une référence à la cellule TxtPinX par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowTextXForm** <br/> |
| **Index de la cellule :**  <br/> |**visXFormPinX** <br/> |
   

