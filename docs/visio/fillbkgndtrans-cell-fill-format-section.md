---
title: FillBkgndTrans, cellule (section Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253230
localization_priority: Normal
ms.assetid: 87065350-ba9a-aae8-47f6-f263f6700d08
description: Détermine le degré de transparence de la couleur d'arrière-plan (remplissage) du motif de remplissage de la forme.
ms.openlocfilehash: 64c5d09fb18f089769e025893b9fac8b1878fca1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423208"
---
# <a name="fillbkgndtrans-cell-fill-format-section"></a>FillBkgndTrans, cellule (section Fill Format)

Détermine le degré de transparence de la couleur d'arrière-plan (remplissage) du motif de remplissage de la forme.
  
|**Valeur**|**Description**|
|:-----|:-----|
|0 - 100  <br/> |Représente le pourcentage de transparence. La valeur par défaut est 0 % (entièrement opaque).  <br/> |
   
## <a name="remarks"></a>Remarques

Les valeurs sont arrondies au demi-point le plus proche. Une valeur de 100 % est complètement transparente. Bien qu'une forme au remplissage complètement transparent apparaisse sur la page de dessin comme une forme sans remplissage, ses effets sur les autres objets de la page seront les mêmes que si elle était complètement opaque.
  
Vous pouvez également définir cette valeur à l’aide du curseur dans la boîte de dialogue **Remplissage** (sous l’onglet **Accueil**, dans le groupe **Forme**, cliquez sur **Remplissage**, puis cliquez sur **Options de remplissage**). Cette valeur contrôle à la fois les transparences de l’ombre de l’arrière-plan et du premier plan. Pour les définir de façon indépendante, vous devez les entrer dans la fenêtre Feuille ShapeSheet.
  
Pour obtenir une référence à la cellule FillBkgndTrans par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |FillBkgndTrans  <br/> |
   
Pour obtenir une référence à la cellule FillBkgndTrans à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**Définis** <br/> |
|Index de la ligne :  <br/> |**visRowFill** <br/> |
|Index de la cellule :  <br/> |**visFillBkgndTrans** <br/> |
   

