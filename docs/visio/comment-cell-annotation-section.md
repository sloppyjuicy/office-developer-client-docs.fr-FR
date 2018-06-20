---
title: Comment, cellule (section Annotation)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60033
localization_priority: Normal
ms.assetid: b367841a-f31c-4b55-4491-2abab5811dbe
description: Contient le texte qui apparaît dans un commentaire.
ms.openlocfilehash: 443a229058a9ca910ba5b38b093706c9c2e3e95b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788274"
---
# <a name="comment-cell-annotation-section"></a>Comment, cellule (section Annotation)

Contient le texte qui apparaît dans un commentaire.
  
> [!NOTE]
> Cette cellule est utilisée pour le suivi des commentaires uniquement lors de l’ouverture d’un fichier .vsd dans Microsoft Visio 2013 ou lors de l’enregistrement d’un fichier .vsdx au format de fichier .vsd. Il n’est pas utilisé pour le suivi des commentaires dans des documents .vsdx dans Visio 2013. 
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Comment par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Annotation.Comment [ *i* ] où *i* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule Comment par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionAnnotation** <br/> |
| Index de la ligne :  <br/> |**visRowAnnotation** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visAnnotationComment** <br/> |
   

