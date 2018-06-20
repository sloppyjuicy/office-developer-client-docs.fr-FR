---
title: ReplaceLockText, cellule (Section de comportement de forme modification)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31f43ebe-3758-4fd9-83b5-775041c5890f
description: Indique si les valeurs des cellules spécifiées dans une forme de remplacent les valeurs (y compris les valeurs locales) d’une forme qui est remplacé pendant une opération de remplacement de forme. Le ReplaceLockText détermine si le texte affiché sur le contrôleur de remplace le texte de la forme remplacée.
ms.openlocfilehash: 75fb0831e7361345f04d7912eb0a55959d9417cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789481"
---
# <a name="replacelocktext-cell-change-shape-behavior-section"></a>ReplaceLockText, cellule (Section de comportement de forme modification)

Indique si les valeurs des cellules spécifiées dans une forme de remplacent les valeurs (y compris les valeurs locales) d’une forme qui est remplacé pendant une opération de remplacement de forme. Le **ReplaceLockText** détermine si le texte affiché sur le contrôleur de remplace le texte de la forme remplacée. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> | Le texte de la forme de base remplace le texte de la forme ancien. En outre, la forme de base remplace les valeurs des cellules dans les sections suivantes lors d’une opération de remplacement de forme :  <br/> Section **Champs de texte**  <br/> Section **Text Block Format**  <br/> |
|FALSE  <br/> |La forme de remplacement contient n’importe quel texte, les champs de texte ou autres propriétés de texte de la forme ancienne qui ont été ajoutées à la forme.  <br/> Lorsque la forme de remplacement contient les propriétés de texte de la forme ancienne, la forme de remplacement a également les valeurs dans les sections de **caractères** et de **paragraphes** de la forme ancienne s’ils disposent de plusieurs lignes.  <br/> |
   
Si la valeur est TRUE (1), les valeurs de la forme principale remplace les valeurs des éléments suivants sur la forme remplacée :
  
- [TheText, cellule (section Events)](thetext-cell-events-section.md)
    
- Cellules de la [Section Character](character-section.md)
    
- Cellules dans la [Section Paragraph](paragraph-section.md)
    
- Cellules dans la [Section Tabs](tabs-section.md)
    
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **ReplaceLockText** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | ReplaceLockText  <br/> |
   
Pour obtenir une référence à la cellule **ReplaceLockText** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowReplaceBehaviors** <br/> |
| Index de la cellule :  <br/> |**visReplaceLockText** <br/> |
   

