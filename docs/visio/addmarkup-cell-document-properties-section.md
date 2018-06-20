---
title: AddMarkup, cellule (section Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030801
localization_priority: Normal
ms.assetid: 46146424-b4c9-2240-36c0-19bb35ec51d1
description: Indique si le document est en révision pour marque de révision.
ms.openlocfilehash: 69430122b0a7665d7daa4a6b28f3a51745b74473
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788022"
---
# <a name="addmarkup-cell-document-properties-section"></a>AddMarkup, cellule (section Document Properties)

Indique si le document est en révision pour marque de révision.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Document en révision.  <br/> |
|FALSE  <br/> |Document pas en révision (valeur par défaut).  <br/> |
   
## <a name="remarks"></a>Remarques

Lorsque la cellule AddMarkup est définie sur TRUE, le réviseur est Ajout de balisage et les modifications sont appliquées aux pages de superposition de balisage, pas aux pages de dessin d’origine. Lorsque la cellule AddMarkup est FALSE, le suivi des révisions est désactivé et les modifications sont appliquées aux pages de dessins d’origine.
  
> [!NOTE]
> Vous pouvez empêcher le balisage dans vos documents à l’aide de la fonction GUARD. Si la cellule AddMarkup contient la formule = GUARD (false), la commande **Suivi des révisions** est désactivée. 
  
Ce paramètre correspond à la valeur de la commande **Suivi des révisions** dans le groupe de **balisage** sous l’onglet **révision** . 
  
Pour obtenir une référence à la cellule AddMarkup par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |AddMarkup  <br/> |
   
Pour obtenir une référence à la cellule AddMarkup par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowDoc** <br/> |
|Index de la cellule :  <br/> |**visDocAddMarkup** <br/> |
   

