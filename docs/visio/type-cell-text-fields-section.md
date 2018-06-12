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
ms.openlocfilehash: 68bfa8a84adb0d46d9621e6fc5383f4b6606f542
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789951"
---
# <a name="type-cell-text-fields-section"></a>Type, cellule (section Text Fields)

Indique un type de données pour la valeur du champ de texte.
  
|**Valeur**|**Description**|
|:-----|:-----|
|0  <br/> |Chaîne  <br/> |
|2  <br/> |Nombre. Inclut les valeurs de date, d'heure, de durée ainsi que les valeurs monétaires, les échelles, les cotes et les angles. Entrez un modèle de format dans la cellule Format.  <br/> |
|5  <br/> |Valeur de date ou d'heure. Affiche les jours, les mois et les années ou les secondes, les minutes et les heures ou encore une date et une heure en même temps. Entrez un modèle de format dans la cellule Format.  <br/> |
|6  <br/> |Valeur de durée. Affiche le temps écoulé. Entrez un modèle de format dans la cellule Format.  <br/> |
|7  <br/> |Valeur monétaire. Utilise les paramètres régionaux actuels de votre système d'exploitation. Entrez un modèle de format dans la cellule Format.  <br/> |
   
## <a name="remarks"></a>Note

Vous pouvez également définir la valeur de cette cellule à l’aide de la boîte de dialogue **champ** (sélectionnez une forme, sous l’onglet **Insertion** , dans le groupe **texte** , cliquez sur **champ** ). 
  
Pour obtenir une référence à la cellule Type par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |Fields.Type [ *i* ] où *i* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule Type par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionTextField** <br/> |
|Index de la ligne :  <br/> |**visRowField** +  *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visFieldType** <br/> |
   

