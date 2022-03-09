---
title: FillPattern, cellule (section Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm375
ms.localizationpriority: medium
ms.assetid: dac82a4f-4508-541a-e118-7d79df987232
description: Détermine le motif de remplissage de la forme. Pour définir un motif de remplissage personnalisé, utilisez la fonction UTILISATION dans cette cellule.
ms.openlocfilehash: 8dc12c8db537e7880e5b77389cd2bcfe6bb926fe
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63404906"
---
# <a name="fillpattern-cell-fill-format-section"></a>FillPattern, cellule (section Fill Format)

Détermine le motif de remplissage de la forme. Pour définir un motif de remplissage personnalisé, utilisez la fonction UTILISATION dans cette cellule.
  
|**Valeur**|**Description**|
|:-----|:-----|
|0  <br/> |Aucun (remplissage transparent). |
|1  <br/> |Couleur d'arrière-plan unie. |
|2 - 40  <br/> |Motifs de remplissage correspondant aux entrées indexées de la boîte de dialogue **Remplir**. |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir cette valeur au moyen de la boîte de dialogue **Remplissage** (sous l’onglet **Accueil**, dans le groupe **Forme**, cliquez sur **Remplissage**, puis cliquez sur **Options de remplissage**).
  
Pour obtenir une référence à la cellule FillPattern par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de la cellule :**  <br/> |FillPattern  <br/> |
   
Pour obtenir une référence à la cellule FillPattern à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRowFill** <br/> |
|**Index de la cellule :**  <br/> |**visFillPattern** <br/> |
   

