---
title: Style, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251249
localization_priority: Normal
ms.assetid: 4372f1e1-f0a9-2f63-ff79-58f2afdceed5
description: Présente la mise en forme de caractères appliquée à une plage de texte dans le bloc de texte de la forme.
ms.openlocfilehash: 48bda5eb798f439e2616b2b910d7ec5ac719d060
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789815"
---
# <a name="style-cell-character-section"></a>Style, cellule (section Character)

Présente la mise en forme de caractères appliquée à une plage de texte dans le bloc de texte de la forme.
  
|**Style**|**Valeur**|**Constante d’Automation**|
|:-----|:-----|:-----|
| Gras  <br/> | &amp;H1  <br/> |**visBold** <br/> |
| Italique  <br/> | &amp;H2  <br/> |**visItalic** <br/> |
| Souligné  <br/> | &amp;H4  <br/> |**visUnderLine** <br/> |
| Petites majuscules  <br/> | &amp;H8  <br/> |**visSmallCaps** <br/> |
   
## <a name="remarks"></a>Note

La cellule Style contient des informations de mise en forme qui sont appliquées à une sous-plage du texte d'une forme si la section Caractère contient plusieurs lignes. Dans le cas contraire, elle contient des informations de mise en forme pour la totalité du texte de la forme.
  
La valeur représente un nombre binaire dans lequel chaque bit indique un style de caractère. Par exemple, une valeur de 3 représente texte mis en forme en gras et en italique. Si la valeur du Style est 0, le texte est normal, sans mise en forme. Vous pouvez tester un format spécifique à l’aide de bits Boolean\* fonctions. Reportez-vous à la documentation pour plus d’informations sur ces fonctions.
  
Pour obtenir une référence à la cellule Style par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Char.Style [ *i* ] où *i* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule Style par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionCharacter** <br/> |
| Index de la ligne :  <br/> |**visRowCharacter** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visCharacterStyle** <br/> |
   
 *Exemple* 
  
Supposons que la cellule Color de la première ligne de la section Character d'une forme soit définie par la formule suivante :
  
= IF(BITAND(Char.Style,1)=1,4,3)
  
Si le premier caractère du texte de la forme est mis en gras, le texte couvert par la première ligne de propriétés Character est bleu (4) ; sinon, il est vert (3). Cet exemple part du principe que les couleurs par défaut sont utilisées.
  
La formule suivante est un exemple de définition de la cellule Style dans un programme. La première instruction fait référence à la cellule Style par son nom et la deuxième, par index. Les deux instructions permettent d'appliquer l'italique au texte couvert par la deuxième ligne de la section Character d'une forme.
  

