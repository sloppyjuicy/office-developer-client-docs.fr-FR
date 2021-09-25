---
title: PageScale, cellule (section Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm775
ms.localizationpriority: medium
ms.assetid: e1da84b3-fd15-12b9-9342-0412e818b3b9
description: Détermine la valeur de l'unité de page dans l'échelle de dessin en cours. L'échelle de dessin est le rapport entre l'unité de page représentée dans la cellule PageScale et l'unité de dessin représentée dans la cellule DrawingScale.
ms.openlocfilehash: 32d596b7b7e2b7e9810f0bc168072eefa534b045
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554221"
---
# <a name="pagescale-cell-page-properties-section"></a>PageScale, cellule (section Page Properties)

Détermine la valeur de l'unité de page dans l'échelle de dessin en cours. L'échelle de dessin est le rapport entre l'unité de page représentée dans la cellule PageScale et l'unité de dessin représentée dans la cellule DrawingScale.
  
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de la cellule PageScale sous l’onglet **Échelle du dessin** dans la boîte de dialogue **Mise en page** (sous l’onglet **Création**, cliquez sur la flèche **Mise en page**). La valeur de la cellule est le premier des deux nombres affichés dans la zone **Échelle prédéfinie** ou **Échelle personnalisée**, selon le paramètre d’échelle de dessin sélectionné sous **Échelle du dessin**. Par exemple, si vous sélectionnez une échelle architecturale pour votre dessin, l’échelle de dessin de la page est de 3/32" = 1’0". La valeur de cellule PageScale est 0,0938 centimètres (ou 3/32") et la valeur de la cellule DrawingScale est de 1 m.
  
Pour obtenir une référence à la cellule PageScale par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |PageScale  <br/> |
   
Pour obtenir une référence à la cellule PageScale à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowPage** <br/> |
|Index de la cellule :  <br/> |**visPageScale** <br/> |
   

