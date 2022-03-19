---
title: TxtWidth, cellule (section Text Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251270
ms.localizationpriority: medium
ms.assetid: e2215c67-25fa-1d75-9cce-f126bb8760a1
description: 'Détermine la largeur du bloc de texte. La formule par défaut est la suivante :'
ms.openlocfilehash: eb6a3616cabe3a4ede9fc34839323c4773f9bde5
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63626842"
---
# <a name="txtwidth-cell-text-transform-section"></a>TxtWidth, cellule (section Text Transform)

Détermine la largeur du bloc de texte. La formule par défaut est la suivante :
  
= Largeur \* 1
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule TxtWidth par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de la cellule :**  <br/> | TxtWidth  <br/> |
   
Pour obtenir une référence à la cellule TxtWidth par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowTextXForm** <br/> |
| **Index de la cellule :**  <br/> |**visXFormWidth** <br/> |
   

