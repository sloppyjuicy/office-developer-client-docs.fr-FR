---
title: EventMultiDrop, cellule (section Events)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f496d698-7f08-69cc-4379-df18a2c2fd7e
ms.openlocfilehash: e44cd18c3f7673761f457db9cd4bfe00a8ab89bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788584"
---
# <a name="eventmultidrop-cell-events-section"></a>EventMultiDrop, cellule (section Events)

Cellule event qui est évaluée lorsque plusieurs formes sont insérées sur la page de dessin en tant qu’instances ou lorsqu’elles sont dupliquées ou collées.
  
Les cellules Event ne sont évaluées que lorsque l'événement se produit, et non lors de l'entrée de la formule.
  
Pour faire référence à la cellule EventMultiDrop par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |EventMultiDrop  <br/> |
   
Pour faire référence à la cellule EventMultiDrop par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowEvent** <br/> |
|Index de la cellule :  <br/> |**visEvtCellMultiDrop** <br/> |
   

