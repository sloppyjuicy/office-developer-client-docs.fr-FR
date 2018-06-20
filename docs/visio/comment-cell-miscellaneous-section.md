---
title: Comment, cellule (section Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm170
localization_priority: Normal
ms.assetid: 6f52ed60-d58b-86e6-f7e2-2ef19d4afa75
description: Contient le texte de commentaire au format chaîne d'une forme.
ms.openlocfilehash: f5222836b29a26cc26ca8093576d0962f0592fae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788281"
---
# <a name="comment-cell-miscellaneous-section"></a>Comment, cellule (section Miscellaneous)

Contient le texte de commentaire au format chaîne d'une forme.
  
## <a name="remarks"></a>Remarques

Vous pouvez également insérer un commentaire en cliquant sur **Nouveau commentaire** sous l’onglet **révision** . 
  
Pour obtenir une référence à la cellule Comment par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |Commentaires  <br/> |
   
Pour obtenir une référence à la cellule Comment par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowMisc** <br/> |
|Index de la cellule :  <br/> |**visComment** <br/> |
   

