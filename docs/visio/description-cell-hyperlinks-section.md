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
ms.openlocfilehash: 567a90b3162c109582c3149c156a994392980577
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788482"
---
# <a name="description-cell-hyperlinks-section"></a>Description, cellule (section Hyperlinks)

Représente une chaîne de texte descriptive d’un lien hypertexte 
  
## <a name="remarks"></a>Remarques

Utilisez cette cellule pour stocker des commentaires sur le lien. Exemple : « Lien vers la page Web de nos tarifs ».
  
Vous pouvez également définir la valeur de cette cellule dans la boîte de dialogue **liens hypertexte** (cliquez sur le **lien hypertexte** sous l’onglet **Insertion** ). 
  
Pour obtenir une référence à la cellule Description par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Lien hypertexte.  *Nom* . Description où un lien hypertexte.  *Nom* est le nom de la ligne hyperlink  <br/> |
   
Pour obtenir une référence à la cellule Description par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionHyperlink** <br/> |
| Index de la ligne :  <br/> |**visRow1stHyperlink** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visHLinkDescription** <br/> |
   

