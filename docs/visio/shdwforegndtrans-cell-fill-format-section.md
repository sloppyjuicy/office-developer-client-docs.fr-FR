---
title: ShdwForegndTrans, cellule (section Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253253
ms.localizationpriority: medium
ms.assetid: c42d4d2e-f8f0-bc5b-6018-4bb4ffa81b64
description: Détermine le niveau de transparence de la couleur utilisée pour le premier plan (trait) du motif de remplissage de l'ombre de la forme.
ms.openlocfilehash: 968127e2c254db545e7ef6deeb7016728cdc3ba0
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62771100"
---
# <a name="shdwforegndtrans-cell-fill-format-section"></a>ShdwForegndTrans, cellule (section Fill Format)

Détermine le niveau de transparence de la couleur utilisée pour le premier plan (trait) du motif de remplissage de l'ombre de la forme.
  
|**Valeur**|**Description**|
|:-----|:-----|
|0 - 100  <br/> |Représente le pourcentage de transparence. La valeur par défaut est 0 % (entièrement opaque). |
   
## <a name="remarks"></a>Remarques

Les valeurs sont arrondies au demi-point le plus proche. Une valeur de 100 % est complètement transparente. Bien qu’une ombre dont le remplissage est entièrement transparent soit identique sur la page de dessin à une ombre sans remplissage, elle interagit avec les autres objets de la page de la même manière que si elle avait une transparence de 0 %.
  
Vous pouvez également définir cette valeur à l’aide du curseur dans la boîte de dialogue **Ombre** (sous l’onglet **Accueil**, dans le groupe **Forme**, cliquez sur **Remplissage**, puis cliquez sur **Options d’ombre**). Cette valeur contrôle à la fois les transparences de l’ombre de l’arrière-plan et du premier plan. Pour les définir de façon indépendante, vous devez les entrer dans la fenêtre Feuille ShapeSheet.
  
Pour obtenir une référence à la cellule ShdwForegndTrans par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |ShdwForegndTrans  <br/> |
   
Pour obtenir une référence à la cellule ShdwForegndTrans par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowFill** <br/> |
|Index de la cellule :  <br/> |**visFillShdwForegndTrans** <br/> |
   

