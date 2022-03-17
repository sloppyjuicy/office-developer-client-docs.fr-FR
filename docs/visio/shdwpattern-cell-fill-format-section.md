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
ms.openlocfilehash: 62672fa05c1a5b7ac4f02f4d8d7ee717ab765837
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63520825"
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
  
||Valeur |
|:-----|:-----|
|**Nom de la cellule :**  <br/> |ShdwPattern  <br/> |
   
Pour obtenir une référence à la cellule ShdwPattern dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRowFill** <br/> |
|**Index de la cellule :**  <br/> |**visFillShdwPattern** <br/> |
   

