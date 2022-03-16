---
title: X, cellule (section Annotation)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1028735
ms.localizationpriority: medium
ms.assetid: f9db8623-9fcf-7037-2d11-d509f463025d
description: Coordonnée x du marqueur de commentaire en coordonnées de page.
ms.openlocfilehash: 2b9c2981fd08c83f73bc55f523668531f96d1a5a
ms.sourcegitcommit: b2c5a02b2d0abd2da2542089fc3f83ff07e121e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2022
ms.locfileid: "63507670"
---
# <a name="x-cell-annotation-section"></a>X, cellule (section Annotation)

Coordonnée *x*  du marqueur de commentaire en coordonnées de page. 
  
> [!NOTE]
> Cette cellule est utilisée pour suivre les commentaires uniquement lors de l’ouverture d’un fichier .vsd dans Microsoft Visio 2013 ou lors de l’enregistrement d’un fichier .vsdx au format de fichier .vsd. Il n’est pas utilisé pour le suivi des commentaires dans les documents .vsdx Visio 2013. 
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule X à l'aide d'un nom à partir d'une autre formule ou programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | Annotation.X[  *i*  ] où  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule X à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionAnnotation** <br/> |
| **Index de la ligne :**  <br/> |**visRowAnnotation** +   *i* où *i* = 0, 1, 2... |
| **Index de la cellule :**  <br/> |**visAnnotationX** <br/> |
   

