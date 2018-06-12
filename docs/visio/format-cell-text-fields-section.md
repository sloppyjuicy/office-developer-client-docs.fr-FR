---
title: Format, cellule (section Text Fields)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm400
localization_priority: Normal
ms.assetid: ab937a00-84c2-6c1c-9080-b7c95ead4f63
description: Détermine la mise en forme d'un champ de texte qui est une chaîne, un nombre, une date ou une heure, une durée ou une devise.
ms.openlocfilehash: 767b658a9431dfab23d2df9bcfa6c83b52f48d75
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788687"
---
# <a name="format-cell-text-fields-section"></a>Format, cellule (section Text Fields)

Détermine la mise en forme d'un champ de texte qui est une chaîne, un nombre, une date ou une heure, une durée ou une devise.
  
## <a name="remarks"></a>Notes

Si la valeur de la cellule Type est 0, 2, 5, 6 ou 7 (chaîne, nombre, date ou heure, durée ou devise, respectivement), spécifiez un modèle de format approprié pour le type de données. Par exemple, le modèle de format « # #/ 4 UU » met en forme les numéros de 12,43 ;. en tant que 12 2/4 pouces. Pour plus d’informations sur la spécification d’un format de l’image, voir [à propos des modèles de format](about-format-pictures.md).
  
Un nombre (Type = 2) peut représenter une cote, un vecteur, un angle, une date, une heure ou une devise. Pour vous assurer qu'un nombre saisi est toujours évalué comme une date, une heure ou une devise, utilisez la fonction DATEHEURE ou CY dans la cellule Format au lieu d'un modèle de format.
  
Pour obtenir une référence à la cellule Format par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Fields.Format [ *i* ] où *i* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule Format par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionTextField** <br/> |
| Index de la ligne :  <br/> |**visRowField** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visFieldFormat** <br/> |
   

