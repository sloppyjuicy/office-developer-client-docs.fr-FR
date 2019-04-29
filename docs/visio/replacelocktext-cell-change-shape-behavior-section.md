---
title: ReplaceLockText Cell (Change Shape Behavior Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31f43ebe-3758-4fd9-83b5-775041c5890f
description: Indique si les valeurs des cellules spécifiées dans une forme de base remplacent les valeurs (y compris les valeurs locales) d'une forme remplacée pendant une opération de remplacement de forme. Le ReplaceLockText détermine si le texte affiché sur la forme de base remplace le texte de la forme remplacée.
ms.openlocfilehash: 299bd571ad935886879abb11108c3d0bd28e3183
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411917"
---
# <a name="replacelocktext-cell-change-shape-behavior-section"></a>ReplaceLockText Cell (Change Shape Behavior Section)

Indique si les valeurs des cellules spécifiées dans une forme de base remplacent les valeurs (y compris les valeurs locales) d'une forme remplacée pendant une opération de remplacement de forme. Le **ReplaceLockText** détermine si le texte affiché sur la forme de base remplace le texte de la forme remplacée. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> | Le texte de la forme de base remplace le texte de l'ancienne forme. En outre, la forme de base remplace les valeurs des cellules dans les sections suivantes lors d'une opération de remplacement de forme:  <br/> Section **champs de texte**  <br/> Section **format de bloc de texte**  <br/> |
|FALSE  <br/> |La forme de remplacement contient du texte, des champs de texte ou d'autres propriétés de texte de l'ancienne forme qui ont été ajoutées à la forme.  <br/> Lorsque la forme de remplacement contient des propriétés de texte de l'ancienne forme, la forme de remplacement a également les valeurs des sections **character** et **paragraph** de l'ancienne forme s'il y a plus d'une ligne.  <br/> |
   
Si la valeur est définie sur TRUE (1), les valeurs de la forme de base remplacent les valeurs des éléments suivants sur la forme remplacée:
  
- [TheText, cellule (section Events)](thetext-cell-events-section.md)
    
- Cellules dans la [section Character](character-section.md)
    
- Cellules dans la [section Paragraph](paragraph-section.md)
    
- Cellules de la [section onglets](tabs-section.md)
    
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **ReplaceLockText** par un nom à partir d'une autre formule, par valeur de l'attribut **N** d'un élément de **cellule** ou d'un programme en faisant appel à la propriété **CellsU** , utilisez: 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | ReplaceLockText  <br/> |
   
Pour obtenir une référence à la cellule **ReplaceLockText** à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants: 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowReplaceBehaviors** <br/> |
| Index de la cellule :  <br/> |**visReplaceLockText** <br/> |
   

