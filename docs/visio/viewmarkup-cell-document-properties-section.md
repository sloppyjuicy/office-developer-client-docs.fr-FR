---
title: ViewMarkup, cellule (section Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030802
ms.localizationpriority: medium
ms.assetid: 6c956266-8266-3312-5a68-cc9d8bdb8cd9
description: Détermine si les marques de révision apparaissent dans la fenêtre de dessin.
ms.openlocfilehash: 85607f120979528f211b7dd3d515f77204446453
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62776857"
---
# <a name="viewmarkup-cell-document-properties-section"></a>ViewMarkup, cellule (section Document Properties)

Détermine si les marques de révision apparaissent dans la fenêtre de dessin. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |La marque de révision est affichée dans le dessin. |
|FALSE  <br/> |La marque de révision n'est pas affichée (valeur par défaut). |
   
## <a name="remarks"></a>Remarques

 Lorsque le suivi des marques de bord est allumé (la cellule AddMarkup a la valeur TRUE), la cellule ViewMarkup est automatiquement définie sur TRUE et reste TRUE même après la désactivée (la cellule AddMarkup a la valeur FALSE). La valeur de la cellule ViewMarkup n'est pas prise en compte lorsque la cellule AddMarkup est définie sur TRUE. 
  
La cellule ViewMarkup est également définie sur TRUE lorsque les commentaires sont insérés dans un dessin (que le suivi des révisions soit activé ou non). Elle doit être également définie sur TRUE pour afficher les commentaires dans le dessin.
  
Cette cellule correspond à la commande **Afficher les marques** dans le groupe **Marques** de l’onglet **Révision**. 
  
Pour obtenir une référence à la cellule ViewMarkup par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |ViewMarkup  <br/> |
   
Pour obtenir une référence à la cellule ViewMarkup à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowDoc** <br/> |
|Index de la cellule :  <br/> |**visDocViewMarkup** <br/> |
   

