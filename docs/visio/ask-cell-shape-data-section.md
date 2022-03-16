---
title: Ask, cellule (section Shape Data)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60
ms.localizationpriority: medium
ms.assetid: b499a5eb-db8f-ebd0-d505-c9a002205e7d
description: Détermine si un utilisateur est invité à entrer les données de forme d’une forme lorsqu’une occurrence est créée ou lorsque la forme est dupliquée ou copiée.
ms.openlocfilehash: beee79d07c2ffa5241720b8ddc60eb9712c9e7e5
ms.sourcegitcommit: b2c5a02b2d0abd2da2542089fc3f83ff07e121e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2022
ms.locfileid: "63506130"
---
# <a name="ask-cell-shape-data-section"></a>Ask, cellule (section Shape Data)

Détermine si un utilisateur est invité à entrer les données de forme d’une forme lorsqu’une occurrence est créée ou lorsque la forme est dupliquée ou copiée.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |L'utilisateur est invité à entrer des données de forme dans la boîte de dialogue **Définir les données de forme**. |
|FALSE  <br/> |L'utilisateur n'est pas invité à entrer de données. |

## <a name="remarks"></a>Remarques

La valeur de cette cellule correspond à la case à cocher **Demander lors de l’insertion** de la boîte de dialogue **Définir les données de forme** (cliquez avec le bouton droit sur la forme, pointez sur **Données**, puis cliquez sur **Définir les données de forme**).
  
Pour obtenir une référence à la cellule Ask par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez :
  
||Valeur |
|:-----|:-----|
|**Nom de cellule :**  <br/> |Prop. *nom* . Vérifiez où Prop. *name est* le nom de la ligne de propriété personnalisée. |

Pour obtenir une référence référence à la cellule Ask à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionProp** <br/> |
|**Index de la ligne :**  <br/> |**visRowProp** +   *i* où *i* = 0, 1, 2,... |
|**Index de la cellule :**  <br/> |**visCustPropsAsk** <br/> |
