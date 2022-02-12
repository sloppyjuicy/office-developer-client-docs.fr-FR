---
title: UICode, cellule (section Text Fields)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1075
ms.localizationpriority: medium
ms.assetid: 1d9717c1-4310-0d62-874f-4df77cd81627
description: Définit le code d'un champ inséré dans les versions de Visio antérieures à Visio 2000.
ms.openlocfilehash: 69337d1bdc74de31377bec4b07fe2418369018ac
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62776843"
---
# <a name="uicode-cell-text-fields-section"></a>UICode, cellule (section Text Fields)

Définit le code d'un champ inséré dans les versions de Visio antérieures à Visio 2000.
  
## <a name="remarks"></a>Remarques

Cette cellule n'apparaît pas dans la fenêtre Feuille ShapeSheet. Utilisez-la pour gérer les problèmes de compatibilité avec les versions précédentes, tels que l'enregistrement au format Visio version 5.0 d'un dessin réalisé dans Visio 2000.
  
Pour obtenir une référence à la cellule UICode par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Fields.UICod[  *i*  ] où  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule UICode par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionTextField** <br/> |
| Index de la ligne :  <br/> |**visRowField** +   *i* où *i* = 0, 1, 2... |
| Index de la cellule :  <br/> |**visFieldUICode** <br/> |
   

