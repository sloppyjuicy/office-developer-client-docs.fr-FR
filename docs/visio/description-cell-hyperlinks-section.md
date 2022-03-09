---
title: Description, cellule (section Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm230
ms.localizationpriority: medium
ms.assetid: 2f571c65-6b7a-5a3a-c075-3c52d3ab989b
description: Représente une chaîne de texte descriptive d’un lien hypertexte
ms.openlocfilehash: 5c6425c796310ff8406a9127420394e4dd60d919
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63404756"
---
# <a name="description-cell-hyperlinks-section"></a>Description, cellule (section Hyperlinks)

Représente une chaîne de texte descriptive d’un lien hypertexte
  
## <a name="remarks"></a>Remarques

Utilisez cette cellule pour stocker des commentaires sur le lien hypertexte . par exemple, « Lien vers notre site web de tarification ».
  
Vous pouvez également définir la valeur de cette cellule dans la boîte de dialogue **Liens hypertexte** (cliquez sur **Liens hypertexte** sous l’onglet **Insertion**).
  
Pour faire référence à la cellule Description par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | Lien hypertexte. *Nom* . Description où Lien hypertexte. *Le* nom est le nom de la ligne de lien hypertexte.  <br/> |

Pour faire référence à la cellule Description à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionHyperlink** <br/> |
| **Index de la ligne :**  <br/> |**visRow1stHyperlink** +  *i*           <br/>où *i* = 0, 1, 2... |
| **Index de la cellule :**  <br/> |**visHLinkDescription** <br/> |
