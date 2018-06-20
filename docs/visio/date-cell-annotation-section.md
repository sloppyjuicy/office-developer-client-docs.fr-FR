---
title: Date, cellule (section Annotation)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60036
localization_priority: Normal
ms.assetid: f1f11803-614b-a40d-0a2d-131093e7609e
description: Contient la date et l'heure du dernier commentaire modifié.
ms.openlocfilehash: 4b6e7ea70302b10728d82f36ad0db39077af9523
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788427"
---
# <a name="date-cell-annotation-section"></a>Date, cellule (section Annotation)

Contient la date et l'heure du dernier commentaire modifié. 
  
> [!NOTE]
> Cette cellule est utilisée pour le suivi des commentaires uniquement lors de l’ouverture d’un fichier .vsd dans Microsoft Visio 2013 ou lors de l’enregistrement d’un fichier .vsdx au format de fichier .vsd. Il n’est pas utilisé pour le suivi des commentaires dans des documents .vsdx dans Visio 2013. 
  
## <a name="remarks"></a>Remarques

Seule la date apparaît dans la zone de commentaires dans l'interface utilisateur.
  
Pour obtenir une référence à la cellule Date par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Annotation.Date [ *i* ] où *i* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule Date par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionAnnotation** <br/> |
| Index de la ligne :  <br/> |**visRowAnnotation** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visAnnotationDate** <br/> |
   

