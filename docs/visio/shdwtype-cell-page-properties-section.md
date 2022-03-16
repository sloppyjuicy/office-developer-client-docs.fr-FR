---
title: ShdwType, cellule (section Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60084
ms.localizationpriority: medium
ms.assetid: 551166d0-3aaa-0fd7-e742-cf3450ba90ed
description: Indique le type d'ombre par défaut d'une page.
ms.openlocfilehash: fbeb7a1714323b8fa9fd5578a9f9f6912c7d7045
ms.sourcegitcommit: b2c5a02b2d0abd2da2542089fc3f83ff07e121e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2022
ms.locfileid: "63506411"
---
# <a name="shdwtype-cell-page-properties-section"></a>ShdwType, cellule (section Page Properties)

Indique le type d'ombre par défaut d'une page.
  
|**Valeur**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
| 1  <br/> | Simple  <br/> |**visFSTSimple** <br/> |
| 2  <br/> | Oblique  <br/> |**visFSTOblique** <br/> |
|3  <br/> |Interne  <br/> |**visFSTInner** <br/> |
   
## <a name="remarks"></a>Remarques

 Le type d’ombre décrit dans cette cellule est utilisé chaque fois que la cellule ShapeShdwType (le type d’ombre d’une forme individuelle sur la page) est définie sur Page Default (**visFSTPageDefault** ). 
  
Les ombres simples sont décrites comme des ombres de décalage dans l'interface utilisateur. Une ombre simple donne l'impression que la forme a son ombre portée sur un plan parallèle situé à une certaine distance derrière elle. Les ombres obliques sont décrites comme telles dans l'interface utilisateur et donnent l'impression d'une ombre portée sur un plan perpendiculaire à la forme. 
  
Pour obtenir une liste des types d’ombre simples et obliques prédéfinis, reportez-vous à la liste **Style** sous l’onglet **Ombres** de la boîte de dialogue **Mise en page** (sous l’onglet **Création**, cliquez sur la flèche **Mise en page**). 
  
Pour obtenir une référence à la cellule ShdwType par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | ShdwType  <br/> |
   
Pour obtenir une référence à la cellule ShdwType par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowPage** <br/> |
| **Index de la cellule :**  <br/> |**visPageShdwType** <br/> |
   

