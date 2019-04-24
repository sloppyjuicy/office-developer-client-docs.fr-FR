---
title: EventMultiDrop, cellule (section Events)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f496d698-7f08-69cc-4379-df18a2c2fd7e
ms.openlocfilehash: caa86e33d0d7aa9ca31cbbf8939e17b581877669
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337190"
---
# <a name="eventmultidrop-cell-events-section"></a>EventMultiDrop, cellule (section Events)

Cellule Event qui est évaluée lorsque plusieurs formes sont déposées sur la page de dessin, soit comme instances, soit lorsque des formes sont dupliquées ou collées.
  
Les cellules événements ne sont évaluées que lorsque l'événement se produit et non lorsque la formule est saisie.
  
Pour faire référence à la cellule EventMultiDrop par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |EventMultiDrop  <br/> |
   
Pour faire référence à la cellule EventMultiDrop par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**Définis** <br/> |
|Index de la ligne :  <br/> |**visRowEvent** <br/> |
|Index de la cellule :  <br/> |**visEvtCellMultiDrop** <br/> |
   

