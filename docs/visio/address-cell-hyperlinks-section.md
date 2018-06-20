---
title: Address, cellule (section Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251387
localization_priority: Normal
ms.assetid: 3864aadd-3f86-c20e-1a74-b0aaff5106f7
description: Indique une adresse d’URL, un nom de fichier ou un chemin d’accès UNC auxquels accéder.
ms.openlocfilehash: 840ce0c4ce73da378f80e5d8a185073ac3915daf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788026"
---
# <a name="address-cell-hyperlinks-section"></a>Address, cellule (section Hyperlinks)

Indique une adresse d’URL, un nom de fichier ou un chemin d’accès UNC auxquels accéder.
  
Vous pouvez spécifier l’adresse comme un chemin d’accès relatif basé sur le chemin d’accès de base défini pour le document dans la zone **base de lien hypertexte** sous l’onglet **Résumé** de la boîte de dialogue **Propriétés** (cliquez sur l’onglet **fichier** , cliquez sur **Info**** propriétés ** puis cliquez sur **Propriétés avancées**). Si le document n’a aucun chemin d’accès de base, l’application utilise le chemin d’accès du document. Si le document n’a pas été enregistré, le lien hypertexte est indéfini.
  
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de la cellule Address dans la boîte de dialogue **liens hypertexte** (cliquez sur le **lien hypertexte** sous l’onglet **Insertion** ). 
  
Pour obtenir une référence à la cellule Address par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |Lien hypertexte. *nom* . Adresse où un lien hypertexte. *nom* est le nom de la ligne hyperlink  <br/> |
   
Pour obtenir une référence à la cellule Address par un nom à partir d’une autre formule ou d’un programme, à l’aide de la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionHyperlink** <br/> |
| Index de la ligne :  <br/> |**visRow1stHyperlink** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visHLinkAddress** <br/> |
   

