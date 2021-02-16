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
ms.openlocfilehash: 0aa270ff918866d8f683a6408ccd71b6a22d555d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426863"
---
# <a name="ask-cell-shape-data-section"></a>Ask, cellule (section Shape Data)

Détermine si un utilisateur est invité à entrer les données de forme d’une forme lorsqu’une occurrence est créée ou lorsque la forme est dupliquée ou copiée.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |L'utilisateur est invité à entrer des données de forme dans la boîte de dialogue **Définir les données de forme**.  <br/> |
|FALSE  <br/> |L'utilisateur n'est pas invité à entrer de données.  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur de cette cellule correspond à la case à cocher **Demander lors de l’insertion** de la boîte de dialogue **Définir les données de forme** (cliquez avec le bouton droit sur la forme, pointez sur **Données**, puis cliquez sur **Définir les données de forme**).
  
Pour obtenir une référence à la cellule Ask par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |Prop. *nom*  . Vérifiez où Prop.  *nom*  est le nom de la ligne de propriété personnalisée.  <br/> |
   
Pour obtenir une référence référence à la cellule Ask à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionProp** <br/> |
|Index de la ligne :  <br/> |**visRowProp**  +   *i* où *i* = 0, 1, 2,...  <br/> |
|Index de la cellule :  <br/> |**visCustPropsAsk** <br/> |
   

