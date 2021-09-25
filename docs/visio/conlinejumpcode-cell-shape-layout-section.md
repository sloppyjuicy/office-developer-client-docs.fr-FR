---
title: ConLineJumpCode, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251652
ms.localizationpriority: medium
ms.assetid: af85588e-8e83-5168-7a8c-d7e8b4af5c27
description: Détermine la déviation des traits de connecteurs.
ms.openlocfilehash: e1caea1f839bb139c41051f288c7e6b160767768
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582910"
---
# <a name="conlinejumpcode-cell-shape-layout-section"></a>ConLineJumpCode, cellule (section Shape Layout)

Détermine la déviation des traits de connecteurs.
  
|**Valeur**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
|0  <br/> |Défini pour la page ; sous l’onglet **Création**, cliquez sur la flèche dans le groupe **Mise en page**, puis cliquez sur sur l’onglet **Disposition et positionnement** pour afficher les spécifications de la page  <br/> |**visSLOJumpDefault** <br/> |
|1  <br/> |Jamais  <br/> |**visSLOJumpNever** <br/> |
|2  <br/> |Toujours  <br/> |**visSLOJumpAlways** <br/> |
|3  <br/> |L'autre connecteur est dévié  <br/> |**visSLOJumpOther** <br/> |
|4   <br/> |Aucun connecteur n'est dévié  <br/> |**visSLOJumpNeither** <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de cette cellule  en sélectionnant un connecteur [](run-in-developer-mode-display-the-developer-tab.md) dynamique, en cliquant sur Comportement dans le groupe Création de forme sous l’onglet Développeur, puis sur l’onglet **Connecteur.**  
  
Pour obtenir une référence à la cellule ConLineJumpCode par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |ConLineJumpCode  <br/> |
   
Pour obtenir une référence à la cellule ConLineJumpCode à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowShapeLayout** <br/> |
|Index de la cellule :  <br/> |**visSLOJumpCode** <br/> |
   

