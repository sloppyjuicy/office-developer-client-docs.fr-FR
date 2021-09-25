---
title: PageLockDuplicate Cell (Page Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: fbaa7d64-06ef-46d6-81d5-9d7af1c14b65
description: Détermine si la page peut être dupliquée, en tant que booléen.
ms.openlocfilehash: 41ac55f68993f164ae7e31aad0aab4720d58643e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562936"
---
# <a name="pagelockduplicate-cell-page-properties-section"></a>PageLockDuplicate Cell (Page Properties Section)

Détermine si la page peut être dupliquée, en tant que booléen.
  
|||
|:-----|:-----|
|TRUE  <br/> |**Les doublons** dans le menu de raccourci de page et la **méthode d’automatisation Page.Duplicate** sont tous deux désactivés pour la page.  <br/> |
|FALSE  <br/> |La page peut être dupliquée.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **PageLockDuplicate** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU,** utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | PageLockDuplicate  <br/> |
   
Pour obtenir une référence à la **cellule PageLockDuplicate** à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowPage** <br/> |
| Index de la cellule :  <br/> |**visPageLockDuplicate** <br/> |
   

