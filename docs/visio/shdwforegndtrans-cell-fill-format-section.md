---
title: ShdwForegndTrans, cellule (section Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253253
localization_priority: Normal
ms.assetid: c42d4d2e-f8f0-bc5b-6018-4bb4ffa81b64
description: Détermine le niveau de transparence de la couleur utilisée pour le premier plan (trait) du motif de remplissage de l'ombre de la forme.
ms.openlocfilehash: 5fd385fc2f46f1ff8eedc961833813ec16ba7b73
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789694"
---
# <a name="shdwforegndtrans-cell-fill-format-section"></a>ShdwForegndTrans, cellule (section Fill Format)

Détermine le niveau de transparence de la couleur utilisée pour le premier plan (trait) du motif de remplissage de l'ombre de la forme.
  
|**Valeur**|**Description**|
|:-----|:-----|
|0 - 100  <br/> |Représente le pourcentage de transparence. La valeur par défaut est 0 % (entièrement opaque).  <br/> |
   
## <a name="remarks"></a>Remarques

Les valeurs sont arrondies au pourcentage le plus proche. Une valeur de 100 % est complètement transparente. Même si une ombre qui possède un remplissage transparent identiques sur la page de dessin apparaît une ombre qui n’est pas remplie, il interagit avec d’autres objets dans la page de la même façon que si sa transparence ont été 0 %.
  
Vous pouvez également définir cette valeur à l’aide du curseur dans la boîte de dialogue **ombre** (sous l’onglet **accueil** , dans le groupe **forme** , cliquez sur **ombre**, puis cliquez sur **Options d’ombres**). Cette valeur contrôle la valeur de l’arrière-plan et premier plan transparents ombre. Pour définir ces valeurs de façon indépendante, vous devez les entrer dans la fenêtre feuille ShapeSheet.
  
Pour obtenir une référence à la cellule ShdwForegndTrans par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |ShdwForegndTrans  <br/> |
   
Pour obtenir une référence à la cellule ShdwForegndTrans par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowFill** <br/> |
|Index de la cellule :  <br/> |**visFillShdwForegndTrans** <br/> |
   

