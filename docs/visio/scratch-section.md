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
ms.openlocfilehash: 16f0bac8f139c0b03d7826ac377a964d15296dd8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789599"
---
# <a name="scratch-section"></a>Scratch, section

Zone de travail dans laquelle vous pouvez entrer et tester des formules auxquelles d'autres cellules sont susceptibles de faire référence.
  
## <a name="remarks"></a>Remarques

Vous pouvez ajouter cette section à l’aide de la boîte de dialogue **Insérer une Section** . Avec le bouton droit dans la fenêtre feuille ShapeSheet, puis cliquez sur **Insérer une Section**.
  
La section **Scratch** est généralement utilisée pour isoler les calculs répétés. Si votre solution a un objectif bien précis, il est préférable d’utiliser une cellule dans la section **User-Defined Cells** pour des raisons de clarté, car les cellules utilisateur peuvent être nommés. 
  
Les cellules dans la section **Scratch** utilisent les unités de deux manières différentes. Les cellules X et Y utilisent les unités de dessin ; N’utilisez pas une cellules D à unités. (Dans le jargon les programmeurs C, les cellules X et Y sont « tapés » et cellules de A à D sont « void ».) Les cellules **Scratch X** et **Y de montage** sont souvent utilisées pour dériver les coordonnées *x* et *y* , telles que **PinX** et **PinY**ou les cellules X et Y d’une cellule de la section **Geometry** . Les cellules de montage Qu'a à D peut afficher toute unité que vous spécifiez. 
  
Une différence supplémentaire est la façon dont ces cellules stockent les valeurs de points. Un point dans Visio est un ensemble de données unique pour une coordonnée ( *x, y*). Lorsqu’une formule renvoie une valeur de point, cette valeur est interprétée dans une des trois manières, selon la formule est dans la cellule de feuille ShapeSheet. Les cellules qui sont associées à *x* -coordonnées (par exemple, **PinX**ou les cellules dans la colonne X d’une section **Geometry** ) extrayez simplement le *x* -coordonner la partie d’une valeur en points. Les cellules liées à *y* -coordonnées extrayez simplement la valeur *y* -coordonner la partie d’une valeur en points. 
  
Par exemple, Visio extrait la formule `PNT(3,4)` ces trois manières. 
  
|**Cell**|**Si vous entrez**|**Visio la traite en tant que**|**Résultat**|
|:-----|:-----|:-----|:-----|
| X   <br/> | `PNT(3,4)` <br/> | `PNTX(PNT(3,4))` <br/> | 76,2000 mm  <br/> |
| Y  <br/> | `PNT(3,4)` <br/> | `PNTY(PNT(3,4))` <br/> | 4,0000 po  <br/> |
| A-D  <br/> | `PNT(3,4)` <br/> | `PNT(3,4)` <br/> | PNT (3.0000 pouces, 4.0000 in.)  <br/> |
   

