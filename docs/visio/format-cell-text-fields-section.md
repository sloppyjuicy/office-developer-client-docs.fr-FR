---
title: Format, cellule (section Text Fields)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm400
ms.localizationpriority: medium
ms.assetid: ab937a00-84c2-6c1c-9080-b7c95ead4f63
description: Détermine la mise en forme d'un champ de texte qui est une chaîne, un nombre, une date ou une heure, une durée ou une devise.
ms.openlocfilehash: 97e49692f33f7ecee44a744002f5a35a2368ece9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598611"
---
# <a name="format-cell-text-fields-section"></a>Format, cellule (section Text Fields)

Détermine la mise en forme d'un champ de texte qui est une chaîne, un nombre, une date ou une heure, une durée ou une devise.
  
## <a name="remarks"></a>Remarques

Si la valeur de la cellule Type est 0, 2, 5, 6 ou 7 (respectivement une chaîne, un nombre, une date ou une heure, une durée ou une devise), indiquez un type de format approprié pour le type de données. Par exemple, le modèle de format « # #/4 UU » fait apparaître le nombre 315,7 mm sous la forme 315 3/4 MILLIMÈTRES. Pour plus d'informations sur la saisie d'un modèle de format, reportez-vous à [À propos des modèles de format](about-format-pictures.md).
  
Un nombre (Type = 2) peut représenter une cote, un vecteur, un angle, une date, une heure ou une devise. Pour vous assurer qu'un nombre saisi est toujours évalué comme une date, une heure ou une devise, utilisez la fonction DATEHEURE ou CY dans la cellule Format au lieu d'un modèle de format.
  
Pour obtenir une référence à la cellule Format par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | Fields.Format[  *i*  ] où  *i*  = <1>, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule Format à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionTextField** <br/> |
| Index de la ligne :  <br/> |**visRowField**  +   *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visFieldFormat** <br/> |
   

