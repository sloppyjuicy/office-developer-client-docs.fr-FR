---
title: QuickStyleShadowColor Cell (Quick Style Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 0a80959f-941f-451c-9049-dc661ff4930f
description: Détermine la couleur de thème que l’ombre d’une forme utilise, sous la forme d’un nombre integer de 0 à 7.
ms.openlocfilehash: 5fc2bff2b47f41e7212bbf21675c67cde2cb6ddd
ms.sourcegitcommit: b2c5a02b2d0abd2da2542089fc3f83ff07e121e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2022
ms.locfileid: "63506704"
---
# <a name="quickstyleshadowcolor-cell-quick-style-section"></a>QuickStyleShadowColor Cell (Quick Style Section)

Détermine la couleur de thème que l’ombre d’une forme utilise, sous la forme d’un nombre integer de 0 à 7.
  
|Valeur |Description |
|:-----|:-----|
|0  <br/> |La couleur d’ombre de forme hérite de la couleur de thème Foncé. |
|1  <br/> |La couleur d’ombre de forme hérite de la couleur de thème Clair. |
|2  <br/> |La couleur d’ombre de forme hérite de la couleur de thème Accent 1. |
|3  <br/> |La couleur d’ombre de forme hérite de la couleur de thème Accent 2. |
|4  <br/> |La couleur d’ombre de forme hérite de la couleur de thème Accent 3. |
|5  <br/> |La couleur d’ombre de forme hérite de la couleur de thème Accent 4. |
|6   <br/> |La couleur d’ombre de forme hérite de la couleur de thème Accent 5. |
|7   <br/> |La couleur d’ombre de forme hérite de la couleur de thème Accent 6. |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **QuickStyleShadowColor** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | QuickStyleShadowColor  <br/> |
   
Pour obtenir une référence à la **cellule QuickStyleShadowColor** à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowQuickStyleProperties** <br/> |
| **Index de la cellule :**  <br/> |**visQuickStyleShadowColor** <br/> |
   

