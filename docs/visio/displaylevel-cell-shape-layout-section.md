---
title: DisplayLevel, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80001
ms.localizationpriority: medium
ms.assetid: 08b730c4-5dd8-106e-ddf3-da2c942e2ef6
description: Détermine la bande du niveau d’affichage (la plage relative de regroupement de l’ordre de plan) pour la forme.
ms.openlocfilehash: 6718c08c9f6b10aaf0ff6da8e4186dfcae524a32
ms.sourcegitcommit: 7b410a51d1e8c97e9cce8d4aa75074162b7d9485
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/12/2022
ms.locfileid: "63448649"
---
# <a name="displaylevel-cell-shape-layout-section"></a>DisplayLevel Cell (Shape Layout Section)

Détermine la bande du niveau d’affichage (la plage relative de regroupement de l’ordre de plan) pour la forme.
  
## <a name="remarks"></a>Remarques

L’ordre de plan est l’ordre d’affichage pour les formes sur la page de dessin. Une forme plus élevée dans l’ordre de plan s’affiche devant une forme plus basse dans l’ordre de plan lorsqu’une des formes chevauche l’autre. 
  
Le niveau d’affichage scinde les formes en regroupements, ou bandes. Toutes les formes d’une bande donnée ont un ordre de plan plus élevé que les formes dans une bande plus basse. Par défaut, la plupart des formes ont un niveau d’affichage de zéro (0).
  
La plage des niveaux d’affichage varie de -32 767 à +32 767. Les formes ayant le même niveau d’affichage sont combinées dans une bande unique, dans laquelle elles sont également classées de manière relative l’une par rapport à l’autre par ordre de plan.
  
Vous pouvez modifier l’ordre de plan des formes au sein d’une bande à l’aide des commandes **Avancer****, Envoyer** vers l’arrière **, Mettre** au premier plan et **Envoyer vers l’arrière**. Si ces commandes déplacent une forme en dehors de sa bande donnée, Microsoft Visio affiche la valeur réservée -32 768 dans la cellule DisplayLevel de la forme, à moins que la cellule ne soit protégée. Dans ce cas, la forme ne peut pas être déplacée sur une autre bande et Visio affiche l’avertissement « La protection de la forme et/ou les propriétés de la couche empêchent de terminer l’exécution de cette commande ». 
  
Pour obtenir une référence à la cellule DisplayLevel par le nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de cellule :**  <br/> |DisplayLevel  <br/> |
   
Pour obtenir une référence à la cellule DisplayLevel à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRowShapeLayout** <br/> |
|**Index de la cellule :**  <br/> |**visSLODisplayLevel** <br/> |
   

