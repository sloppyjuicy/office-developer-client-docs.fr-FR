---
title: Date, cellule (section Annotation)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60036
ms.localizationpriority: medium
ms.assetid: f1f11803-614b-a40d-0a2d-131093e7609e
description: Contient la date et l'heure du dernier commentaire modifié.
ms.openlocfilehash: ec2463b8f2274e5713c0c1b1e13754e399e05c61
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62787386"
---
# <a name="date-cell-annotation-section"></a>Date, cellule (section Annotation)

Contient la date et l'heure du dernier commentaire modifié. 
  
> [!NOTE]
> Cette cellule est utilisée pour suivre les commentaires uniquement lors de l’ouverture d’un fichier .vsd dans Microsoft Visio 2013 ou lors de l’enregistrement d’un fichier .vsdx au format de fichier .vsd. Il n’est pas utilisé pour le suivi des commentaires dans les documents .vsdx Visio 2013. 
  
## <a name="remarks"></a>Remarques

Seule la date apparaît dans la zone de commentaires dans l'interface utilisateur.
  
Pour obtenir une référence à la cellule Date par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Annotation.Date[  *i*  ] où  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule Date à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionAnnotation** <br/> |
| Index de la ligne :  <br/> |**visRowAnnotation** +   *i* où *i* = 0, 1, 2... |
| Index de la cellule :  <br/> |**visAnnotationDate** <br/> |
   

