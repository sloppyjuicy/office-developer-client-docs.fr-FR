---
title: EventMultiDrop, cellule (section Events)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: f496d698-7f08-69cc-4379-df18a2c2fd7e
ms.openlocfilehash: 35d38657048b65263fd932e540d2ca15e8006be2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582728"
---
# <a name="eventmultidrop-cell-events-section"></a>EventMultiDrop, cellule (section Events)

Cellule d’événement évaluée lorsque plusieurs formes sont abandonnées sur la page de dessin, soit en tant qu’instances, soit lorsque des formes sont dupliquées ou copiées.
  
Les cellules événements ne sont évaluées que lorsque l'événement se produit et non lorsque la formule est saisie.
  
Pour faire référence à la cellule EventMultiDrop par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |EventMultiDrop  <br/> |
   
Pour faire référence à la cellule EventMultiDrop par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowEvent** <br/> |
|Index de la cellule :  <br/> |**visEvtCellMultiDrop** <br/> |
   

