---
title: Type, cellule (section Text Fields)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1060
localization_priority: Normal
ms.assetid: 69d64520-9a47-07ca-09c7-d1e5da620348
description: Indique un type de données pour la valeur du champ de texte.
ms.openlocfilehash: 91a2d60133d9a39e152656558f168742a5409883
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358925"
---
# <a name="type-cell-text-fields-section"></a>Type, cellule (section Text Fields)

Indique un type de données pour la valeur du champ de texte.
  
|**Value**|**Description**|
|:-----|:-----|
|0  <br/> |Chaîne.  <br/> |
|n°2  <br/> |Nombre. Inclut les valeurs de date, d'heure, de durée ainsi que les valeurs monétaires, les échelles, les cotes et les angles. Entrez un modèle de format dans la cellule Format.  <br/> |
|disque  <br/> |Valeur de date ou d'heure. Affiche les jours, les mois et les années ou les secondes, les minutes et les heures ou encore une date et une heure en même temps. Entrez un modèle de format dans la cellule Format.  <br/> |
|6.x  <br/> |Valeur de durée. Affiche le temps écoulé. Entrez un modèle de format dans la cellule Format.  <br/> |
|7j/7  <br/> |Valeur monétaire. Utilise les paramètres régionaux actuels de votre système d'exploitation. Entrez un modèle de format dans la cellule Format.  <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de cette cellule à l'aide de la boîte de dialogue **champ** (avec une forme sélectionnée, sous l'onglet **insertion** , dans le groupe **texte** , cliquez sur **champ** ). 
  
Pour obtenir une référence à la cellule Type par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |Fields. type [ *i* ] où *i* = <1>, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule Type par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionTextField** <br/> |
|Index de la ligne :  <br/> |**visRowField** +  *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visFieldType** <br/> |
   

