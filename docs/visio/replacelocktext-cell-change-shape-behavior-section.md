---
title: ReplaceLockText Cell (Change Shape Behavior Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 31f43ebe-3758-4fd9-83b5-775041c5890f
description: Indique si les valeurs des cellules spécifiées dans une forme de base remplacent les valeurs d’une forme en cours de remplacement lors d’une opération de remplacement de forme.
ms.openlocfilehash: 31a9333aab0fd88a55ab580a36d25355c4301f27
ms.sourcegitcommit: 138c9e15adc07c6ecd740257872aaee6a1a1a7fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64406357"
---
# <a name="replacelocktext-cell-change-shape-behavior-section"></a>ReplaceLockText Cell (Change Shape Behavior Section)

Indique si les valeurs des cellules spécifiées dans une forme de base remplacent les valeurs (y compris les valeurs locales) d’une forme remplacée lors d’une opération de remplacement de forme. **ReplaceLockText détermine** si le texte affiché sur la forme de maître remplace le texte de la forme en cours de remplacement. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> | Le texte de la forme de maître le sur-place sur l’ancienne forme. En outre, la forme de base remplace les valeurs des cellules des sections suivantes lors d’une opération de remplacement de forme :  <br/> **Section Champs de** texte  <br/> **Section Format de bloc de** texte  <br/> |
|FALSE  <br/> |La forme de remplacement contient du texte, des champs de texte ou d’autres propriétés de texte de l’ancienne forme qui ont été ajoutées à la forme. Lorsque la forme de remplacement contient des propriétés de texte de l’ancienne forme, la forme de remplacement possède également les valeurs des sections **Character** et **Paragraph** de l’ancienne forme si elles contiennent plusieurs lignes. |
   
Si la valeur TRUE (1) est définie, les valeurs de la forme master remplacent les valeurs suivantes sur la forme en cours de remplacement :
  
- [TheText, cellule (section Events)](thetext-cell-events-section.md)
    
- Cellules de la [section Character](character-section.md)
    
- Cellules de la [section Paragraph](paragraph-section.md)
    
- Cellules de la [section Tabs](tabs-section.md)
    
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **ReplaceLockText** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | ReplaceLockText  <br/> |
   
Pour obtenir une référence à la **cellule ReplaceLockText** à l’aide d’un index à partir d’un programme, utilisez la **propriété CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowReplaceBehaviors** <br/> |
| **Index de la cellule :**  <br/> |**visReplaceLockText** <br/> |
   

