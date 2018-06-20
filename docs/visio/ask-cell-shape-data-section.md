---
title: Ask, cellule (section Shape Data)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60
localization_priority: Normal
ms.assetid: b499a5eb-db8f-ebd0-d505-c9a002205e7d
description: Détermine si un utilisateur est invité à entrer les données de forme d’une forme lorsqu’une occurrence est créée ou lorsque la forme est dupliquée ou copiée.
ms.openlocfilehash: 94e84be4bef5c8c13d5c8ef5108ab89b71f251b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788016"
---
# <a name="ask-cell-shape-data-section"></a>Ask, cellule (section Shape Data)

Détermine si un utilisateur est invité à entrer les données de forme d’une forme lorsqu’une occurrence est créée ou lorsque la forme est dupliquée ou copiée.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Demandez à l’utilisateur à entrer des données de forme dans la boîte de dialogue **Définir les données de forme** .  <br/> |
|FALSE  <br/> |N’est pas invité à entrer des données utilisateur.  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur de cette cellule correspond à la case à cocher **Demander lors de l’insertion** dans la boîte de dialogue **Définir les données de forme** (avec le bouton droit de la forme, pointez sur **données**, puis cliquez sur **Définir les données de forme**).
  
Pour obtenir une référence à la cellule Ask par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |Propriétés. *nom* . Vérifiez où de propriétés.  *nom* est le nom de la ligne de propriété personnalisée.  <br/> |
   
Pour obtenir une référence à la cellule Ask par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionProp** <br/> |
|Index de la ligne :  <br/> |**visRowProp** +  *i* où *i* = 0, 1, 2,...  <br/> |
|Index de la cellule :  <br/> |**visCustPropsAsk** <br/> |
   

