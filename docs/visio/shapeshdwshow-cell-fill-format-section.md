---
title: ShapeShdwShow, cellule (Section Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ece6c889-9291-40ea-b55a-072acdcb8a52
description: Détermine si la forme affiche une ombre, comme un entier compris entre 0 et 2.
ms.openlocfilehash: 72077e60089acd3cd3f8a9349691e1468f6b1f9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789667"
---
# <a name="shapeshdwshow-cell-fill-format-section"></a>ShapeShdwShow, cellule (Section Fill Format)

Détermine si la forme affiche une ombre, comme un entier compris entre 0 et 2.
  
|**Valeur**|**Description**|
|:-----|:-----|
|0  <br/> |Toujours afficher l’ombre si une ombre est spécifiée. Les ombres pour sous-formes ne sont pas affichées.  <br/> |
|1  <br/> |Ne s’affichent pas une ombre, sauf si la forme n’a pas de parent. Utilisez les ombres sous forme si regroupés.  <br/> |
|2  <br/> |Toujours afficher une ombre si une ombre est spécifiée. Les ombres pour les formes secondaires sont affichées.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **ShapeShdwShow** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | ShapeShdwShow  <br/> |
   
Pour obtenir une référence à la cellule **ShapeShdwShow** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowFill** <br/> |
| Index de la cellule :  <br/> |**visFillShdwShow** <br/> |
   

