---
title: ShdwPattern, cellule (section Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm935
localization_priority: Normal
ms.assetid: eca73b80-9835-9011-1dce-187ccee92e76
description: Détermine le motif de remplissage de l'ombre d'une forme.
ms.openlocfilehash: fd24a8d23d62436a6d81cf6b8049dcabe47db677
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789701"
---
# <a name="shdwpattern-cell-fill-format-section"></a>ShdwPattern, cellule (section Fill Format)

Détermine le motif de remplissage de l'ombre d'une forme.
  
|**Valeur**|**Description**|
|:-----|:-----|
|0  <br/> |Aucun (remplissage transparent).  <br/> |
|1  <br/> |Couleur de premier plan unie  <br/> |
|2 - 40  <br/> |Motifs assortis  <br/> |
   
## <a name="remarks"></a>Remarques

Pour définir le motif de remplissage, entrez un numéro à partir de 0 à 40, qui est un index dans une collection de modèles. Vous pouvez afficher l’ensemble des motifs de remplissage dans la boîte de dialogue **remplissage** (sous l’onglet **accueil** , dans le groupe **forme** , cliquez sur **remplissage**, puis cliquez sur **Options de remplissage**).
  
Pour obtenir une référence à la cellule ShdwPattern par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |ShdwPattern  <br/> |
   
Pour obtenir une référence à la cellule ShdwPattern par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowFill** <br/> |
|Index de la cellule :  <br/> |**visFillShdwPattern** <br/> |
   

