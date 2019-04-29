---
title: ShapeShdwShow Cell (Fill Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ece6c889-9291-40ea-b55a-072acdcb8a52
description: Détermine si la forme affiche une ombre, sous la forme d'un nombre entier compris entre 0 et 2.
ms.openlocfilehash: 1da52c20acaa19eab79970a751fad2c225e212ae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422116"
---
# <a name="shapeshdwshow-cell-fill-format-section"></a>ShapeShdwShow Cell (Fill Format Section)

Détermine si la forme affiche une ombre, sous la forme d'un nombre entier compris entre 0 et 2.
  
|**Valeur**|**Description**|
|:-----|:-----|
|0  <br/> |Affiche toujours l'ombre si une ombre est spécifiée. Les ombres des sous-formes ne sont pas affichées.  <br/> |
|0,1  <br/> |Ne pas afficher d'ombre, sauf si la forme n'a pas de parent. Utiliser des ombres de sous-formes si elles sont regroupées.  <br/> |
|n°2  <br/> |Affiche toujours une ombre si une ombre est spécifiée. Les ombres des sous-formes sont affichées.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **ShapeShdwShow** par un nom à partir d'une autre formule, par valeur de l'attribut **N** d'un élément de **cellule** ou d'un programme en faisant appel à la propriété **CellsU** , utilisez: 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | ShapeShdwShow  <br/> |
   
Pour obtenir une référence à la cellule **ShapeShdwShow** à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants: 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowFill** <br/> |
| Index de la cellule :  <br/> |**visFillShdwShow** <br/> |
   

