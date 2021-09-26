---
title: UICategory, cellule (section Text Fields)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1070
ms.localizationpriority: medium
ms.assetid: 365f7005-ba34-2311-4c5c-16344962fc3f
description: Définit la catégorie d'un champ inséré dans les versions de Visio antérieures à Visio 2000.
ms.openlocfilehash: c7733b73338fabee3759169cce9374f8d56bbf1e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627220"
---
# <a name="uicategory-cell-text-fields-section"></a>UICategory, cellule (section Text Fields)

Définit la catégorie d'un champ inséré dans les versions de Visio antérieures à Visio 2000.
  
## <a name="remarks"></a>Remarques

Cette cellule n'apparaît pas dans la fenêtre Feuille ShapeSheet. Utilisez-la pour gérer les problèmes de compatibilité avec les versions précédentes, tels que l'enregistrement au format Visio 5.0 d'un dessin réalisé dans Visio 2000.
  
Pour obtenir une référence à la cellule UICategory par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Fields.UICat[  *i*  ] où  *i*  = <1>, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule UICategory par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionTextField** <br/> |
| Index de la ligne :  <br/> |**visRowField**  +   *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visFieldUICategory** <br/> |
   

