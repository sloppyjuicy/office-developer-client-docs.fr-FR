---
title: LineColorTrans, cellule (section Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50120
ms.localizationpriority: medium
ms.assetid: b68054b5-7efd-1156-9dc1-5ec94e18d227
description: Détermine le niveau de transparence de la couleur de trait d'une forme.
ms.openlocfilehash: a0ce88d932e3b4a6b0cf52d5dcad1333703f549e
ms.sourcegitcommit: b2c5a02b2d0abd2da2542089fc3f83ff07e121e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2022
ms.locfileid: "63506028"
---
# <a name="linecolortrans-cell-line-format-section"></a>LineColorTrans, cellule (section Line Format)

Détermine le niveau de transparence de la couleur de trait d'une forme.
  
|**Valeur**|**Description**|
|:-----|:-----|
|0 - 100  <br/> |Représente le pourcentage de transparence. La valeur par défaut est 0 % (entièrement opaque). |
   
## <a name="remarks"></a>Remarques

Les valeurs sont arrondies au pourcentage le plus proche. Une valeur de 100 % correspond à une transparence totale. Même si une forme dont la couleur de trait est entièrement transparente apparaît identique à une forme dépourvue de traits sur la page de dessin, elle interagit avec les autres objets de la page de la même façon que si elle avait une transparence de 0 %. 
  
Vous pouvez également définir cette valeur à l’aide du curseur dans la boîte de dialogue **Trait** (sous l’onglet **Accueil**, dans le groupe **Forme**, cliquez sur **Trait**, pointez sur **Poids**, puis cliquez sur **Autres traits**).
  
Pour obtenir une référence à la cellule LineColorTrans par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de la cellule :**  <br/> |LineColorTrans  <br/> |
   
Pour obtenir une référence à la cellule LineColorTrans à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRowLine** <br/> |
|**Index de la cellule :**  <br/> |**visLineColorTrans** <br/> |
   

