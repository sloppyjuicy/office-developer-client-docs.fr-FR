---
title: PageLockDuplicate Cell (Page Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: fbaa7d64-06ef-46d6-81d5-9d7af1c14b65
description: Détermine si la page peut être dupliquée, en tant que booléen.
ms.openlocfilehash: e3f0be543631e267fd0c4796be99b76dce7dfd84
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62784656"
---
# <a name="pagelockduplicate-cell-page-properties-section"></a>PageLockDuplicate Cell (Page Properties Section)

Détermine si la page peut être dupliquée, en tant que booléen.
  
|||
|:-----|:-----|
|TRUE  <br/> |**Le** doublon dans le menu de raccourci de page et la **méthode d’automatisation Page.Duplicate** sont tous deux désactivés pour la page. |
|FALSE  <br/> |La page peut être dupliquée. |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **PageLockDuplicate** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | PageLockDuplicate  <br/> |
   
Pour obtenir une référence à la **cellule PageLockDuplicate** à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowPage** <br/> |
| Index de la cellule :  <br/> |**visPageLockDuplicate** <br/> |
   

