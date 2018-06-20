---
title: Y, cellule (section Annotation)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60095
localization_priority: Normal
ms.assetid: 527a4615-2013-a4b4-81cd-7f5d71c1803c
description: La valeur y-coordonnées de la marque de commentaire en coordonnées de page.
ms.openlocfilehash: cc2399de7919512796a39ca39c705c214f4c51a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790071"
---
# <a name="y-cell-annotation-section"></a>Y, cellule (section Annotation)

La valeur *y* -coordonnées de la marque de commentaire en coordonnées de page. 
  
> [!NOTE]
> Cette cellule est utilisée pour le suivi des commentaires uniquement lors de l’ouverture d’un fichier .vsd dans Microsoft Visio 2013 ou lors de l’enregistrement d’un fichier .vsdx au format de fichier .vsd. Il n’est pas utilisé pour le suivi des commentaires dans des documents .vsdx dans Visio 2013. 
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Y par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Annotation.Y [ *i* ] où *i* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule Y par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionAnnotation** <br/> |
| Index de la ligne :  <br/> |**visRowAnnotation** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visAnnotationY** <br/> |
   

