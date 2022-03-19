---
title: TxtLocPinY, cellule (section Text Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251276
ms.localizationpriority: medium
ms.assetid: 3f46cfcf-7eac-4a37-e782-39f4e7f8fc43
description: 'Détermine la coordonnée y du centre de rotation du bloc de texte par rapport à l’origine du bloc de texte. La formule par défaut est la suivante :'
ms.openlocfilehash: 13ab82cde12460fbe4391aa98843e56bf0030e3c
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63627906"
---
# <a name="txtlocpiny-cell-text-transform-section"></a>TxtLocPinY, cellule (section Text Transform)

Détermine la coordonnée  *y*  du centre de rotation du bloc de texte par rapport à l’origine du bloc de texte. La formule par défaut est la suivante : 
  
= TxtHeight \* 0.5
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule TxtLocPinY par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de la cellule :**  <br/> | TxtLocPinY  <br/> |
   
Pour obtenir une référence à la cellule TxtLocPinY par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowTextXForm** <br/> |
| **Index de la cellule :**  <br/> |**visXFormLocPinY** <br/> |
   

