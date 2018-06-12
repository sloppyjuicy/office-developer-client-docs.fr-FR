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
ms.openlocfilehash: 26429e06ad432eaf7fae9188ac676cb4be3201c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788634"
---
# <a name="fillpattern-cell-fill-format-section"></a>FillPattern, cellule (section Fill Format)

Détermine le motif de remplissage de la forme. Pour définir un motif de remplissage personnalisé, utilisez la fonction UTILISATION dans cette cellule.
  
|**Valeur**|**Description**|
|:-----|:-----|
|0  <br/> |Aucun (remplissage transparent).  <br/> |
|1  <br/> |Couleur d'arrière-plan unie.  <br/> |
|2 - 40  <br/> |Motifs de remplissage correspondant aux entrées indexées de la boîte de dialogue **remplissage** .  <br/> |
   
## <a name="remarks"></a>Note

Vous pouvez également définir cette valeur à l’aide de la boîte de dialogue **remplissage** (sous l’onglet **accueil** , dans le groupe **forme** , cliquez sur **remplissage** , puis sur **Options de remplissage**).
  
Pour obtenir une référence à la cellule FillPattern par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |FillPattern  <br/> |
   
Pour obtenir une référence à la cellule FillPattern par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowFill** <br/> |
|Index de la cellule :  <br/> |**visFillPattern** <br/> |
   

