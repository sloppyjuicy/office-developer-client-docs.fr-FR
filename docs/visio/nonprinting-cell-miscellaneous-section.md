---
title: NonPrinting, cellule (section Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251321
localization_priority: Normal
ms.assetid: 59fe0887-2092-4fad-ea38-2aba354f3b92
description: Active ou désactive l'impression de la forme sélectionnée.
ms.openlocfilehash: ab00914a9c59cfe94b3f7273f89684f43328b4d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789168"
---
# <a name="nonprinting-cell-miscellaneous-section"></a>NonPrinting, cellule (section Miscellaneous)

Active ou désactive l'impression de la forme sélectionnée.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | L'impression est désactivée mais la forme est affichée dans la fenêtre de dessin.  <br/> |
| FALSE  <br/> | L'impression est activée.  <br/> |
   
## <a name="remarks"></a>Notes

Pour imprimer un repère, sélectionnez-le, puis affectez la valeur FALSE à la cellule NonPrinting.
  
Pour obtenir une référence à la cellule NonPrinting par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | NonPrinting  <br/> |
   
Pour obtenir une référence à la cellule NonPrinting par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowMisc** <br/> |
| Index de la cellule :  <br/> |**visNonPrinting** <br/> |
   

