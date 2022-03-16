---
title: Y, cellule (section Annotation)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60095
ms.localizationpriority: medium
ms.assetid: 527a4615-2013-a4b4-81cd-7f5d71c1803c
description: Coordonnée y de la marque de commentaire en coordonnées de page.
ms.openlocfilehash: 15307790feb93f20dbff02437509c01e11a9076e
ms.sourcegitcommit: b2c5a02b2d0abd2da2542089fc3f83ff07e121e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2022
ms.locfileid: "63506149"
---
# <a name="y-cell-annotation-section"></a>Y, cellule (section Annotation)

Coordonnée *y*  de la marque de commentaire en coordonnées de page. 
  
> [!NOTE]
> Cette cellule est utilisée pour suivre les commentaires uniquement lors de l’ouverture d’un fichier .vsd dans Microsoft Visio 2013 ou lors de l’enregistrement d’un fichier .vsdx au format de fichier .vsd. Il n’est pas utilisé pour le suivi des commentaires dans les documents .vsdx Visio 2013. 
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Y à l'aide d'un nom à partir d'une autre formule ou programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | Annotation.Y [  *i*  ] où  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule Y à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionAnnotation** <br/> |
| **Index de la ligne :**  <br/> |**visRowAnnotation** +   *i* où *i* = 0, 1, 2... |
| **Index de la cellule :**  <br/> |**visAnnotationY** <br/> |
   

