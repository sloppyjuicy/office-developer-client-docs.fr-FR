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
ms.openlocfilehash: bc996d9fa07c11b0493184284d1280e848745c61
ms.sourcegitcommit: b2c5a02b2d0abd2da2542089fc3f83ff07e121e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2022
ms.locfileid: "63507375"
---
# <a name="format-cell-text-fields-section"></a>Format, cellule (section Text Fields)

Détermine la mise en forme d'un champ de texte qui est une chaîne, un nombre, une date ou une heure, une durée ou une devise.
  
## <a name="remarks"></a>Remarques

Si la valeur de la cellule Type est 0, 2, 5, 6 ou 7 (respectivement une chaîne, un nombre, une date ou une heure, une durée ou une devise), indiquez un type de format approprié pour le type de données. Par exemple, le modèle de format « # #/4 UU » fait apparaître le nombre 315,7 mm sous la forme 315 3/4 MILLIMÈTRES. Pour plus d'informations sur la saisie d'un modèle de format, reportez-vous à [À propos des modèles de format](about-format-pictures.md).
  
Un nombre (Type = 2) peut représenter une cote, un vecteur, un angle, une date, une heure ou une devise. Pour vous assurer qu'un nombre saisi est toujours évalué comme une date, une heure ou une devise, utilisez la fonction DATEHEURE ou CY dans la cellule Format au lieu d'un modèle de format.
  
Pour obtenir une référence à la cellule Format par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | Fields.Format[  *i*  ] où  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule Format à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionTextField** <br/> |
| **Index de la ligne :**  <br/> |**visRowField** +   *i* où *i* = 0, 1, 2... |
| **Index de la cellule :**  <br/> |**visFieldFormat** <br/> |
   

