---
title: UICategory, cellule (section Text Fields)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1070
localization_priority: Normal
ms.assetid: 365f7005-ba34-2311-4c5c-16344962fc3f
description: Définit la catégorie d'un champ inséré dans les versions de Visio antérieures à Visio 2000.
ms.openlocfilehash: fc060ac1533732749d10e1855dc3841602051520
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789968"
---
# <a name="uicategory-cell-text-fields-section"></a>UICategory, cellule (section Text Fields)

Définit la catégorie d'un champ inséré dans les versions de Visio antérieures à Visio 2000.
  
## <a name="remarks"></a>Note

Cette cellule n'apparaît pas dans la fenêtre Feuille ShapeSheet. Utilisez-la pour gérer les problèmes de compatibilité avec les versions précédentes, tels que l'enregistrement au format Visio 5.0 d'un dessin réalisé dans Visio 2000.
  
Pour obtenir une référence à la cellule UICategory par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Fields.UICat [ *i* ] où *i* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule UICategory par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionTextField** <br/> |
| Index de la ligne :  <br/> |**visRowField** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visFieldUICategory** <br/> |
   

