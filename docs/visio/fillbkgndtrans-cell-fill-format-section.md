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
ms.openlocfilehash: c8dcec8cc0bdb87700bb85754298ec4755bae7d0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788624"
---
# <a name="fillbkgndtrans-cell-fill-format-section"></a>FillBkgndTrans, cellule (section Fill Format)

Détermine le degré de transparence de la couleur d'arrière-plan (remplissage) du motif de remplissage de la forme.
  
|**Valeur**|**Description**|
|:-----|:-----|
|0 - 100  <br/> |Représente le pourcentage de transparence. La valeur par défaut est 0 % (entièrement opaque).  <br/> |
   
## <a name="remarks"></a>Note

Les valeurs sont arrondies au demi-point le plus proche. Une valeur de 100 % est complètement transparente. Bien qu'une forme au remplissage complètement transparent apparaisse sur la page de dessin comme une forme sans remplissage, ses effets sur les autres objets de la page seront les mêmes que si elle était complètement opaque.
  
Vous pouvez également définir cette valeur à l’aide du curseur dans la boîte de dialogue **remplissage** (sous l’onglet **accueil** , dans le groupe **forme** , cliquez sur **remplissage**, puis cliquez sur **Options de remplissage**). Cette valeur contrôle la valeur de transparence de remplissage de l’arrière-plan et de premier plan. Pour définir ces valeurs de façon indépendante, vous devez les entrer dans la fenêtre feuille ShapeSheet.
  
Pour obtenir une référence à la cellule FillBkgndTrans par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |FillBkgndTrans  <br/> |
   
Pour obtenir une référence à la cellule FillBkgndTrans par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowFill** <br/> |
|Index de la cellule :  <br/> |**visFillBkgndTrans** <br/> |
   

