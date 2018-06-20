---
title: PageLockDuplicate, cellule (Section Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fbaa7d64-06ef-46d6-81d5-9d7af1c14b65
description: Détermine si la page peut être dupliquée, comme une valeur booléenne.
ms.openlocfilehash: 6cfe8f7a33942f51130ef103b8aba70a5c38b37d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789204"
---
# <a name="pagelockduplicate-cell-page-properties-section"></a>PageLockDuplicate, cellule (Section Page Properties)

Détermine si la page peut être dupliquée, comme une valeur booléenne.
  
|||
|:-----|:-----|
|TRUE  <br/> |**En double** dans le menu contextuel de page et la méthode d’automation **Page.Duplicate** sont tous deux désactivés pour la page.  <br/> |
|FALSE  <br/> |La page peut être dupliquée.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **PageLockDuplicate** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | PageLockDuplicate  <br/> |
   
Pour obtenir une référence à la cellule **PageLockDuplicate** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowPage** <br/> |
| Index de la cellule :  <br/> |**visPageLockDuplicate** <br/> |
   

