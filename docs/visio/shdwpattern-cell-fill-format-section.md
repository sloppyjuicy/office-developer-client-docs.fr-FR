---
title: ShdwPattern, cellule (section Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm935
ms.localizationpriority: medium
ms.assetid: eca73b80-9835-9011-1dce-187ccee92e76
description: Détermine le motif de remplissage de l'ombre d'une forme.
ms.openlocfilehash: 2216cc18149cf36be52b3c034d8c0634fa40e9b8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559543"
---
# <a name="shdwpattern-cell-fill-format-section"></a>ShdwPattern, cellule (section Fill Format)

Détermine le motif de remplissage de l'ombre d'une forme.
  
|**Valeur**|**Description**|
|:-----|:-----|
|0  <br/> |Aucun (remplissage transparent).  <br/> |
|1  <br/> |Couleur de premier plan unie  <br/> |
|2 - 40  <br/> |Motifs assortis  <br/> |
   
## <a name="remarks"></a>Remarques

Pour définir le motif de remplissage, entrez une valeur comprise entre 0 et 40, correspondant à un index d’un ensemble de motifs. Vous pouvez afficher cet index dans la boîte de dialogue **Remplissage** (sous l’onglet **Accueil**, dans le groupe **Forme**, cliquez sur **Remplissage**, puis cliquez sur **Options de remplissage**).
  
Pour obtenir une référence à la cellule ShdwPattern par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |ShdwPattern  <br/> |
   
Pour obtenir une référence à la cellule ShdwPattern dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowFill** <br/> |
|Index de la cellule :  <br/> |**visFillShdwPattern** <br/> |
   

