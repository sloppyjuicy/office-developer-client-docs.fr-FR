---
title: Comment, cellule (section Annotation)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60033
ms.localizationpriority: medium
ms.assetid: b367841a-f31c-4b55-4491-2abab5811dbe
description: Contient le texte qui apparaît dans un commentaire.
ms.openlocfilehash: b6dc406a6fcc7a49332db88cee0acb40ba6373a5
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63630314"
---
# <a name="comment-cell-annotation-section"></a>Comment, cellule (section Annotation)

Contient le texte qui apparaît dans un commentaire.
  
> [!NOTE]
> Cette cellule est utilisée pour suivre les commentaires uniquement lors de l’ouverture d’un fichier .vsd dans Microsoft Visio 2013 ou lors de l’enregistrement d’un fichier .vsdx au format de fichier .vsd. Il n’est pas utilisé pour le suivi des commentaires dans les documents .vsdx Visio 2013. 
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Comment par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | Annotation.Comment[  *i*  ] où  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule Comment à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionAnnotation** <br/> |
| **Index de la ligne :**  <br/> |**visRowAnnotation** +   *i* où *i* = 0, 1, 2... |
| **Index de la cellule :**  <br/> |**visAnnotationComment** <br/> |
   

