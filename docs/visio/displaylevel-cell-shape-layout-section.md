---
title: DisplayLevel, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80001
localization_priority: Normal
ms.assetid: 08b730c4-5dd8-106e-ddf3-da2c942e2ef6
description: Détermine la bande du niveau d’affichage (la plage relative de regroupement de l’ordre de plan) pour la forme.
ms.openlocfilehash: 516446b2d401aaca614e24a2c5bb5003fafe8574
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788459"
---
# <a name="displaylevel-cell-shape-layout-section"></a>DisplayLevel, cellule (section Shape Layout)

Détermine la bande du niveau d’affichage (la plage relative de regroupement de l’ordre de plan) pour la forme.
  
## <a name="remarks"></a>Note

L’ordre de plan est l’ordre d’affichage pour les formes sur la page de dessin. Une forme plus élevée dans l’ordre de plan s’affiche devant une forme plus basse dans l’ordre de plan lorsqu’une des formes chevauche l’autre. 
  
Le niveau d’affichage scinde les formes en regroupements, ou bandes. Toutes les formes d’une bande donnée ont un ordre de plan plus élevé que les formes dans une bande plus basse. Par défaut, la plupart des formes ont un niveau d’affichage de zéro (0).
  
La plage des niveaux d’affichage varie de -32 767 à +32 767. Les formes ayant le même niveau d’affichage sont combinées dans une bande unique, dans laquelle elles sont également classées de manière relative l’une par rapport à l’autre par ordre de plan.
  
Vous pouvez modifier l’ordre de plan des formes dans une bande en utilisant les commandes **Avancer**, **Reculer**, **mettre au premier plan**et **mettre à l’arrière-plan**. Si ces commandes déplacement une forme de sa bande donnée, Microsoft Visio affiche la valeur réservée -32768 dans la cellule DisplayLevel de la forme, sauf si la cellule est protégée. Dans ce cas, la forme ne peut pas être déplacée vers une autre bande et Visio affiche l’avertissement « propriétés de forme protection et/ou layer empêchent l’exécution de cette commande. » 
  
Pour obtenir une référence à la cellule DisplayLevel par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |DisplayLevel  <br/> |
   
Pour obtenir une référence à la cellule DisplayLevel par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowShapeLayout** <br/> |
|Index de la cellule :  <br/> |**visSLODisplayLevel** <br/> |
   

