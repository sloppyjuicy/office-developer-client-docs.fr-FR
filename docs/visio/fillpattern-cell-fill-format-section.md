---
title: FillPattern, cellule (section Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm375
localization_priority: Normal
ms.assetid: dac82a4f-4508-541a-e118-7d79df987232
description: Détermine le motif de remplissage de la forme. Pour définir un motif de remplissage personnalisé, utilisez la fonction UTILISATION dans cette cellule.
ms.openlocfilehash: 340ccdc9f3819fb29e210832107e270bd302433c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322434"
---
# <a name="fillpattern-cell-fill-format-section"></a>FillPattern, cellule (section Fill Format)

Détermine le motif de remplissage de la forme. Pour définir un motif de remplissage personnalisé, utilisez la fonction UTILISATION dans cette cellule.
  
|**Value**|**Description**|
|:-----|:-----|
|0  <br/> |Aucun (remplissage transparent).  <br/> |
|0,1  <br/> |Couleur d'arrière-plan unie.  <br/> |
|2 - 40  <br/> |Motifs de remplissage correspondant aux entrées indexées de la boîte de dialogue **Remplir**.  <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir cette valeur au moyen de la boîte de dialogue **Remplissage** (sous l’onglet **Accueil**, dans le groupe **Forme**, cliquez sur **Remplissage**, puis cliquez sur **Options de remplissage**).
  
Pour obtenir une référence à la cellule FillPattern par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |FillPattern  <br/> |
   
Pour obtenir une référence à la cellule FillPattern à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**Définis** <br/> |
|Index de la ligne :  <br/> |**visRowFill** <br/> |
|Index de la cellule :  <br/> |**visFillPattern** <br/> |
   

