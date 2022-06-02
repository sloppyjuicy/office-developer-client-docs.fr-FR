---
title: Scratch, section
description: Décrit les remarques de la section Scratch, qui est une zone de travail permettant d’entrer et de tester des formules qui peuvent être référencées par d’autres cellules.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm2125
ms.localizationpriority: medium
ms.assetid: 144dd06f-7225-57db-fd19-a58d6bccf0e1
ms.openlocfilehash: 0a0b176f26d759134ddbb184bb0171f423c50192
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65852704"
---
# <a name="scratch-section"></a>Scratch Section

Zone de travail dans laquelle vous pouvez entrer et tester des formules auxquelles d'autres cellules sont susceptibles de faire référence.
  
## <a name="remarks"></a>Remarques

Vous pouvez ajouter cette section à l’aide de la boîte de dialogue **Insérer une section**. Cliquez avec le bouton droit dans la fenêtre Feuille ShapeSheet, puis cliquez sur **Insérer une section**.
  
La section **Scratch** est généralement utilisée pour isoler les calculs complexes répétés. Si votre solution a un objectif bien défini, il est plus judicieux d’utiliser une cellule dans la section **Cellules définies par l’utilisateur** pour plus de clarté, car les cellules utilisateur peuvent être nommées.
  
Les cellules de la section **Scratch** utilisent des unités de deux manières différentes. Les cellules X et Y utilisent les unités de dessin ; les cellules de A à D n’utilisent pas d’unité. (Dans le jargon des programmeurs C, les cellules X et Y sont « typées », et les cellules A à D sont « void ». Les cellules **Scratch X** et **Scratch Y** sont souvent utilisées pour dérivation des coordonnées *x* et *y* , telles que **PinX** et **PinY**, ou les cellules X et Y trouvées dans une cellule de section **Geometry** . Les cellules Scratch de A à D peuvent afficher toute unité que vous spécifiez.
  
L'autre différence entre ces cellules tient à la façon dont les valeurs des points sont stockées. Un point dans Visio est un package de données unique pour une coordonnée ( *x,y*). Lorsqu'une formule renvoie une valeur de point, cette valeur est interprétée selon l'une des trois méthodes, suivant la cellule ShapeSheet dans laquelle se trouve la formule. Les cellules liées aux coordonnées *x* (par exemple, **PinX** ou les cellules de la colonne X d’une section **Geometry** ) extraient uniquement la partie *x-coordonnées* d’une valeur de point. Les cellules qui se rapportent aux coordonnées *y* extraient *uniquement la partie* y-coordonnées d’une valeur de point.
  
Par exemple, Visio extrait la formule `PNT(3,4)` de ces trois manières.
  
|**Cell**|**Si vous entrez**|**Visio la traite en tant que**|**Résultat**|
|:-----|:-----|:-----|:-----|
| X  <br/> | `PNT(3,4)` <br/> | `PNTX(PNT(3,4))` <br/> | 76,2000 mm |
| v  <br/> | `PNT(3,4)` <br/> | `PNTY(PNT(3,4))` <br/> | 4,0000 po |
| A-D  <br/> | `PNT(3,4)` <br/> | `PNT(3,4)` <br/> | PNT(3.0000 pouces, 4.0000 pouces.)  <br/> |
