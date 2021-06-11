---
title: PageLockDuplicate Cell (Page Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fbaa7d64-06ef-46d6-81d5-9d7af1c14b65
description: Détermine si la page peut être dupliquée, en tant que booléen.
ms.openlocfilehash: 8ce730fcdc2dff5deac44d8c053b84e82a82d4cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425980"
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
   

