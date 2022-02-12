---
title: Default, cellule (section Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251545
ms.localizationpriority: medium
ms.assetid: 0edea0ea-58dd-15da-6d4f-185d40133452
description: Détermine le lien hypertexte par défaut d'une forme ou d'une page. Définissez la valeur de cette cellule comme TRUE pour définir un lien hypertexte par défaut.
ms.openlocfilehash: ebe783729f1f3600d4bc6926cc77758dc934bdef
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62775954"
---
# <a name="default-cell-hyperlinks-section"></a>Default, cellule (section Hyperlinks)

Détermine le lien hypertexte par défaut d'une forme ou d'une page. Définissez la valeur de cette cellule comme TRUE pour définir un lien hypertexte par défaut.
  
## <a name="remarks"></a>Remarques

Vous pouvez également définir le lien hypertexte par défaut en sélectionnant une forme et en cliquant sur **Lien hypertexte** sous l’onglet **Insertion**, en sélectionnant ensuite un lien hypertexte, puis en cliquant sur **Par défaut**. Le lien hypertexte par défaut s’affiche en texte gras.
  
Pour obtenir une référence à la cellule Default par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |Lien hypertexte. *Nom*  . Par défaut où Lien hypertexte. *Le nom*  est le nom de la ligne  <br/> |
   
Pour obtenir une référence à la cellule Default à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionHyperlink** <br/> |
|Index de la ligne :  <br/> |**visRow1stHyperlink** +   *i* où *i* = 0, 1, 2... |
|Index de la cellule :  <br/> |**visHLinkDefault** <br/> |
   

