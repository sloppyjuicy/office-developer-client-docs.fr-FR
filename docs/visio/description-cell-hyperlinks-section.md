---
title: Description, cellule (section Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm230
localization_priority: Normal
ms.assetid: 2f571c65-6b7a-5a3a-c075-3c52d3ab989b
description: Représente une chaîne de texte descriptive d’un lien hypertexte
ms.openlocfilehash: b58e6dc3ec2fc3b64db00e0f19e0718fe897aaa3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396623"
---
# <a name="description-cell-hyperlinks-section"></a>Cellule Description (section Liens hypertexte)

Représente une chaîne de texte descriptive d’un lien hypertexte 
  
## <a name="remarks"></a>Remarques

Utilisez cette cellule pour stocker des commentaires sur le lien hypertexte. par exemple, « un lien vers notre site prix. »
  
Vous pouvez également définir la valeur de cette cellule dans la boîte de dialogue **Liens hypertexte** (cliquez sur **Liens hypertexte** sous l’onglet **Insertion**). 
  
Pour faire référence à la cellule Description par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Lien hypertexte.  *Nom* . Description où un lien hypertexte.  *Nom* est le nom de la ligne hyperlink  <br/> |
   
Pour faire référence à la cellule Description à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionHyperlink** <br/> |
| Index de la ligne :  <br/> |**visRow1stHyperlink** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visHLinkDescription** <br/> |
   

