---
title: ViewMarkup, cellule (section Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030802
localization_priority: Normal
ms.assetid: 6c956266-8266-3312-5a68-cc9d8bdb8cd9
description: Détermine si les marques de révision apparaissent dans la fenêtre de dessin.
ms.openlocfilehash: dda908595b243878ec755cf73351ec1fd672dc55
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790026"
---
# <a name="viewmarkup-cell-document-properties-section"></a>ViewMarkup, cellule (section Document Properties)

Détermine si les marques de révision apparaissent dans la fenêtre de dessin. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |La marque de révision est affichée dans le dessin.  <br/> |
|FALSE  <br/> |La marque de révision n'est pas affichée (valeur par défaut).  <br/> |
   
## <a name="remarks"></a>Note

 Lorsque le suivi des révisions sont activée (cellule AddMarkup a la valeur TRUE), la cellule ViewMarkup est automatiquement définie sur TRUE et conserve la valeur TRUE même une fois que le suivi des révisions a été désactivée (cellule AddMarkup a la valeur FALSE). La valeur de la cellule ViewMarkup est ignorée lorsque la cellule AddMarkup est définie sur TRUE. 
  
La cellule ViewMarkup est également définie sur TRUE lorsque les commentaires sont insérés dans un dessin (que le suivi des révisions soit activé ou non). Elle doit être également définie sur TRUE pour afficher les commentaires dans le dessin.
  
Cette cellule correspond à la commande **Afficher les marques** dans le groupe de **balisage** sous l’onglet **révision** . 
  
Pour obtenir une référence à la cellule ViewMarkup par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |ViewMarkup  <br/> |
   
Pour obtenir une référence à la cellule ViewMarkup par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowDoc** <br/> |
|Index de la cellule :  <br/> |**visDocViewMarkup** <br/> |
   

