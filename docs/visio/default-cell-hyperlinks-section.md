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
ms.openlocfilehash: 3b3be465fb896ffd04701df1ddc10d0044aeb7b2
ms.sourcegitcommit: 4164855836af53a068bbbc5b5d126f83ee83e324
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2022
ms.locfileid: "63426803"
---
# <a name="default-cell-hyperlinks-section"></a>Default, cellule (section Hyperlinks)

Détermine le lien hypertexte par défaut d'une forme ou d'une page. Définissez la valeur de cette cellule comme TRUE pour définir un lien hypertexte par défaut.
  
## <a name="remarks"></a>Remarques

Vous pouvez également définir le lien hypertexte par défaut en sélectionnant une forme et en cliquant sur **Lien hypertexte** sous l’onglet **Insertion**, en sélectionnant ensuite un lien hypertexte, puis en cliquant sur **Par défaut**. Le lien hypertexte par défaut s’affiche en texte gras.
  
Pour obtenir une référence à la cellule Default par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de cellule :**  <br/> |Lien hypertexte. *Nom*  . Par défaut où Lien hypertexte. *Le nom*  est le nom de la ligne  <br/> |
   
Pour obtenir une référence à la cellule Default à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionHyperlink** <br/> |
|**Index de la ligne :**  <br/> |**visRow1stHyperlink** +   *i* où *i* = 0, 1, 2... |
|**Index de la cellule :**  <br/> |**visHLinkDefault** <br/> |
   

