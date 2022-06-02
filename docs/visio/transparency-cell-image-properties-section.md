---
title: Transparency, cellule (section Image Properties)
description: Décrit les remarques de la cellule Transparency (section Propriétés de l’image), qui détermine le niveau de transparence d’une couleur de couche.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm51095
ms.localizationpriority: medium
ms.assetid: 5b265356-1602-4241-fbe1-4d5a55392a52
ms.openlocfilehash: 3e57587a00c421697fcd0eee1a338948690f8d34
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65852095"
---
# <a name="transparency-cell-image-properties-section"></a>Transparency, cellule (section Image Properties)

Définit le niveau de transparence de la couleur d'un calque.
  
|**Valeur**|**Description**|
|:-----|:-----|
|0 - 100  <br/> |Représente le pourcentage de transparence. La valeur par défaut est 0 % (entièrement opaque). |
   
## <a name="remarks"></a>Remarques

Les valeurs sont arrondies au demi-point le plus proche. Une valeur de 100 % correspond à une transparence totale. Même si un calque dont la couleur est entièrement transparente apparaît identique sur la page de dessin à un calque dépourvu de couleur, il interagit avec les autres objets de la page de la même façon que s’il avait une transparence de 0 %. Vous pouvez également définir cette valeur à l’aide du curseur dans la boîte de dialogue **Propriétés des calques** (sous l’onglet **Accueil**, dans le groupe **Modification**, cliquez sur **Calques**, puis cliquez sur **Propriétés des calques**).
  
Pour obtenir une référence à la cellule Transparency par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de la cellule :**  <br/> |Transparence  <br/> |
   
Pour obtenir une référence à la cellule Transparency par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRowImage** <br/> |
|**Index de la cellule :**  <br/> |**visImageTransparency** <br/> |
   

