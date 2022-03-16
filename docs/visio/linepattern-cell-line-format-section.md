---
title: LinePattern, cellule (section Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm560
ms.localizationpriority: medium
ms.assetid: a416762b-7294-c99f-d9f1-332c3ed35dff
description: Détermine le motif de trait d'une forme. La valeur entrée dans la cellule LinePattern est un nombre correspondant à un index d'un ensemble de motifs de trait.
ms.openlocfilehash: 2a5d5225cc713d5b30dad086edcf4d85869b6121
ms.sourcegitcommit: b2c5a02b2d0abd2da2542089fc3f83ff07e121e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2022
ms.locfileid: "63507293"
---
# <a name="linepattern-cell-line-format-section"></a>LinePattern, cellule (section Line Format)

Détermine le motif de trait d'une forme. La valeur entrée dans la cellule LinePattern est un nombre correspondant à un index d'un ensemble de motifs de trait.
  
|**Valeur**|**Description**|
|:-----|:-----|
|0  <br/> |Aucun motif de trait  <br/> |
|1  <br/> |Solid  <br/> |
|2 - 23  <br/> |Motifs de trait assortis  <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez afficher l’ensemble des motifs de trait dans la boîte de dialogue **Trait** (sous l’onglet **Accueil**, dans le groupe **Forme**, cliquez sur **Trait**, pointez sur **Tirets**, puis cliquez sur **Autres traits**).
  
Pour choisir un motif de trait personnalisé, utilisez la fonction USE dans cette cellule.
  
Pour obtenir une référence à la cellule LinePattern par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de la cellule :**  <br/> |LinePattern  <br/> |
   
Pour obtenir une référence à la cellule LinePattern à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRowLine** <br/> |
|**Index de la cellule :**  <br/> |**visLinePattern** <br/> |
   

