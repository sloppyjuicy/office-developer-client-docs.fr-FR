---
title: Address, cellule (section Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251387
ms.localizationpriority: medium
ms.assetid: 3864aadd-3f86-c20e-1a74-b0aaff5106f7
description: Indique une adresse d’URL, un nom de fichier ou un chemin d’accès UNC auxquels accéder.
ms.openlocfilehash: ef893335b25fb400cbfc1f153a3fcdcd7a66be02
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578290"
---
# <a name="address-cell-hyperlinks-section"></a>Address, cellule (section Hyperlinks)

Indique une adresse d’URL, un nom de fichier ou un chemin d’accès UNC auxquels accéder.
  
Vous pouvez spécifier l’adresse comme chemin d’accès relatif basé sur  le chemin d’accès de base  défini pour le document dans la zone de **base Lien hypertexte** de l’onglet Résumé de la boîte de dialogue Propriétés (cliquez sur l’onglet Fichier, cliquez sur **Info,** sur ** Propriétés **, puis sur **Propriétés** avancées).  Si le document n’a pas de chemin de base, l’application utilise le chemin d’accès du document. Si le document n’a pas encore été enregistré, le lien hypertexte n’est pas défini.
  
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de la cellule Address dans la boîte de dialogue **Liens hypertexte** (cliquez sur **Lien hypertexte** sous l’onglet **Insertion**). 
  
Pour obtenir une référence à la cellule Address à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |Lien hypertexte. *nom*  . Adresse où Hyperlink. *nom*  est le nom de la ligne de lien hypertexte  <br/> |
   
Pour obtenir une référence à la cellule Address par un nom à partir d’une autre formule ou d’un programme, à l’aide de la propriété **CellsU,** utilisez : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionHyperlink** <br/> |
| Index de la ligne :  <br/> |**visRow1stHyperlink**  +   *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visHLinkAddress** <br/> |
   

