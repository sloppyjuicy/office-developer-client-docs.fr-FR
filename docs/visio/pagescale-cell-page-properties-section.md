---
title: PageScale, cellule (section Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm775
localization_priority: Normal
ms.assetid: e1da84b3-fd15-12b9-9342-0412e818b3b9
description: Détermine la valeur de l'unité de page dans l'échelle de dessin en cours. L'échelle de dessin est le rapport entre l'unité de page représentée dans la cellule PageScale et l'unité de dessin représentée dans la cellule DrawingScale.
ms.openlocfilehash: 0e1721ea667ad3bcd9f35880ab4e63bc90802c32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789247"
---
# <a name="pagescale-cell-page-properties-section"></a>PageScale, cellule (section Page Properties)

Détermine la valeur de l'unité de page dans l'échelle de dessin en cours. L'échelle de dessin est le rapport entre l'unité de page représentée dans la cellule PageScale et l'unité de dessin représentée dans la cellule DrawingScale.
  
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de la cellule PageScale sous l’onglet **À l’échelle de dessin** dans la boîte de dialogue **Mise en Page** (sous l’onglet **Création** , cliquez sur la flèche **Mise en Page** ). La valeur de la cellule est le premier des deux nombres dans la zone **échelle prédéfinie** ou **échelle personnalisée** , selon le paramètre à l’échelle de dessin sélectionné sous **échelle du dessin**. Par exemple, si vous sélectionnez une échelle architecturale pour votre dessin, l’échelle de la page de dessin est 3/32 "= 1'0". La valeur de la cellule PageScale est en 0.0938. (ou 3/32") et la valeur de la cellule DrawingScale est ft 1.
  
Pour obtenir une référence à la cellule PageScale par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |PageScale  <br/> |
   
Pour obtenir une référence à la cellule PageScale par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowPage** <br/> |
|Index de la cellule :  <br/> |**visPageScale** <br/> |
   

