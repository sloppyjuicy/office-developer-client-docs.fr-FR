---
title: FillForegndTrans, cellule (section Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253231
localization_priority: Normal
ms.assetid: 8b1b3904-6635-3fd1-31a9-ff32c19394af
description: Détermine le degré de transparence de la couleur de premier plan dans le motif de remplissage de la forme.
ms.openlocfilehash: d05a83f83ea3d95ac3d42a2bfb3996917119f580
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322448"
---
# <a name="fillforegndtrans-cell-fill-format-section"></a>FillForegndTrans, cellule (section Fill Format)

Détermine le degré de transparence de la couleur de premier plan dans le motif de remplissage de la forme.
  
|**Value**|**Description**|
|:-----|:-----|
|0 - 100  <br/> |Représente le pourcentage de transparence. La valeur par défaut est 0 % (entièrement opaque).  <br/> |
   
## <a name="remarks"></a>Remarques

Les valeurs sont arrondies au demi-point le plus proche. Une valeur de 100 % est complètement transparente. Bien qu'une forme au remplissage complètement transparent apparaisse sur la page de dessin comme une forme sans remplissage, ses effets sur les autres objets de la page seront les mêmes que si elle était complètement opaque.
  
Vous pouvez également définir cette valeur à l’aide du curseur dans la boîte de dialogue **Remplissage** (sous l’onglet **Accueil**, dans le groupe **Forme**, cliquez sur **Remplissage**, puis cliquez sur **Options de remplissage**). Cette valeur contrôle à la fois les transparences de l’ombre de l’arrière-plan et du premier plan. Pour les définir de façon indépendante, vous devez les entrer dans la fenêtre Feuille ShapeSheet.
  
Pour obtenir une référence à la cellule FillForegndTrans par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |FillForegndTrans  <br/> |
   
Pour obtenir une référence à la cellule FillForegndTrans à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**Définis** <br/> |
|Index de la ligne :  <br/> |**visRowFill** <br/> |
|Index de la cellule :  <br/> |**visFillForegndTrans** <br/> |
   

