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
ms.openlocfilehash: 4e0860639b0d89fce2c35a8947bd5ac00fcc63e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427632"
---
# <a name="addmarkup-cell-document-properties-section"></a>AddMarkup, cellule (section Document Properties)

Indique si le document est en révision pour marque de révision.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Document en révision.  <br/> |
|FALSE  <br/> |Document pas en révision (valeur par défaut).  <br/> |
   
## <a name="remarks"></a>Remarques

Lorsque la cellule AddMarkup est définie sur TRUE, le réviseur ajoute une marque de révision et des modifications sont apportées pour marquer les pages qui se superposent, pas les pages de dessin d'origine. Lorsque la cellule AddMarkup est définie sur FALSE, le suivi des révisions est désactivé et les modifications sont appliquées aux pages de dessin d'origine.
  
> [!NOTE]
> Vous pouvez empêcher le markup sur vos documents à l’aide de la fonction GUARD. Si la cellule AddMarkup contient la formule =GUARD(FALSE), la commande **De** suivi est désactivée. 
  
Ce paramètre correspond à la commande **Suivi des révisions** dans le groupe **Marque de révision** de l’onglet **Révision**. 
  
Pour obtenir une référence à la cellule AddMarkup par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |AddMarkup  <br/> |
   
Pour obtenir une référence à la cellule AddMarkup à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowDoc** <br/> |
|Index de la cellule :  <br/> |**visDocAddMarkup** <br/> |
   

