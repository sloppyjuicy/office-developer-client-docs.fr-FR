---
title: Description, cellule (section Action Tags)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60037
ms.localizationpriority: medium
ms.assetid: feb29b91-0f6e-6353-3dd0-7a280843a517
description: Contient une chaîne qui décrit la balise d’action, qui s’affiche sous forme d’info-bulle lorsque l’utilisateur place le pointeur sur la balise.
ms.openlocfilehash: b9c7c45ab703fb3dd4869be3d0b679a9f50b30b0
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63406139"
---
# <a name="description-cell-action-tags-section"></a>Description Cell (Action Tags Section)

Contient une chaîne qui décrit la balise d’action, qui s’affiche sous forme d’info-bulle lorsque l’utilisateur place le pointeur sur la balise.
  
## <a name="remarks"></a>Remarques

Pour faire référence à la cellule Description par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | SmartTags.  *nom*  . Description où SmartTags. *name est*  le nom de la ligne de balise d’action  <br/> |
   
Pour faire référence à la cellule Description à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionSmartTag** <br/> |
| **Index de la ligne :**  <br/> |**visRowSmartTag** +   *i* où *i* = 0, 1, 2... |
| **Index de la cellule :**  <br/> |**visSmartTagDescription** <br/> |
   

