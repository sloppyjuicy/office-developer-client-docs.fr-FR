---
title: Scratch, section
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm2125
localization_priority: Normal
ms.assetid: 144dd06f-7225-57db-fd19-a58d6bccf0e1
description: Zone de travail dans laquelle vous pouvez entrer et tester des formules auxquelles d'autres cellules sont susceptibles de faire référence.
ms.openlocfilehash: a7d2c6762e96fc19986521c2ba164666b925c928
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344526"
---
# <a name="scratch-section"></a>Scratch Section

Zone de travail dans laquelle vous pouvez entrer et tester des formules auxquelles d'autres cellules sont susceptibles de faire référence.
  
## <a name="remarks"></a>Remarques

Vous pouvez ajouter cette section à l’aide de la boîte de dialogue **Insérer une section**. Cliquez avec le bouton droit dans la fenêtre Feuille ShapeSheet, puis cliquez sur **Insérer une section**.
  
La section **Scratch** est généralement utilisée pour isoler les calculs complexes répétés. Si votre solution a un objectif bien défini, il est judicieux d'utiliser une cellule de la section **cellules définies** par l'utilisateur pour des raisons de clarté, car les cellules utilisateur peuvent être nommées. 
  
Les cellules de la section **Scratch** utilisent des unités de deux manières différentes. Les cellules X et Y utilisent les unités de dessin ; les cellules de A à D n’utilisent pas d’unité. (Dans le jargon du programmeur C, les cellules X et Y sont «tapées» et les cellules de A à D sont «vides».) Les cellules **Scratch x** et **Scratch Y** sont souvent utilisées pour dériver les coordonnées *x* et *y* , telles que **PinX** et **PinY**, ou les cellules X et y figurant dans une cellule de la section **Geometry** . Les cellules Scratch de A à D peuvent afficher toute unité que vous spécifiez. 
  
L'autre différence entre ces cellules tient à la façon dont les valeurs des points sont stockées. Un point dans Visio est un package de données unique pour une coordonnée ( *x, y*). Lorsqu'une formule renvoie une valeur de point, cette valeur est interprétée selon l'une des trois méthodes, suivant la cellule ShapeSheet dans laquelle se trouve la formule. Les cellules associées à des coordonnées *x* (par exemple, **PinX**, ou les cellules de la colonne x d' **** une section Geometry) extraient uniquement la partie de coordonnée *x* d'une valeur de point. Les cellules liées aux coordonnées *y* extraient uniquement la partie de la coordonnée *y* d'une valeur de point. 
  
Par exemple, Visio extrait la formule `PNT(3,4)` de trois façons. 
  
|**Cell**|**Si vous entrez**|**Visio la traite en tant que**|**Résultat**|
|:-----|:-----|:-----|:-----|
| X  <br/> | `PNT(3,4)` <br/> | `PNTX(PNT(3,4))` <br/> | 76,2000 mm  <br/> |
| v  <br/> | `PNT(3,4)` <br/> | `PNTY(PNT(3,4))` <br/> | 4,0000 po  <br/> |
| A-D  <br/> | `PNT(3,4)` <br/> | `PNT(3,4)` <br/> | PNT (3.0000, 4,0000)  <br/> |
   

