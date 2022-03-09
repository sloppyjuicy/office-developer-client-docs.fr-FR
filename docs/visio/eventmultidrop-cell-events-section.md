---
title: EventMultiDrop, cellule (section Events)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: f496d698-7f08-69cc-4379-df18a2c2fd7e
ms.openlocfilehash: 57a14e0b56fff2776423dbc0e68d5aacc314473f
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63403450"
---
# <a name="eventmultidrop-cell-events-section"></a>EventMultiDrop, cellule (section Events)

Cellule d’événement évaluée lorsque plusieurs formes sont abandonnées sur la page de dessin, en tant qu’instances ou lorsque des formes sont dupliquées ou copiées.
  
Les cellules événements ne sont évaluées que lorsque l'événement se produit et non lorsque la formule est saisie.
  
Pour faire référence à la cellule EventMultiDrop par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de la cellule :**  <br/> |EventMultiDrop  <br/> |
   
Pour faire référence à la cellule EventMultiDrop par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :

 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRowEvent** <br/> |
|**Index de la cellule :**  <br/> |**visEvtCellMultiDrop** <br/> |
   

