---
title: Address, cellule (section Hyperlinks)
manager: lindalu
ms.date: 03/09/2022
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251387
ms.localizationpriority: medium
ms.assetid: 3864aadd-3f86-c20e-1a74-b0aaff5106f7
description: Indique une adresse d’URL, un nom de fichier ou un chemin d’accès UNC auxquels accéder.
ms.openlocfilehash: 745b9a4cc233bf59db832d0d75ac76d33c136a63
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63405636"
---
# <a name="address-cell-hyperlinks-section"></a>Address, cellule (section Hyperlinks)

Indique une adresse d’URL, un nom de fichier ou un chemin d’accès UNC auxquels accéder.
  
Vous pouvez spécifier l’adresse comme chemin d’accès relatif basé sur le chemin d’accès de base défini pour le  document dans la zone de  **base Lien hypertexte** de  l’onglet Résumé de la boîte de dialogue Propriétés (cliquez sur l’onglet Fichier, sur **Informations**, sur Propriétés **, puis** sur **Propriétés** avancées). Si le document n’a pas de chemin de base, l’application utilise le chemin d’accès du document. Si le document n’a pas encore été enregistré, le lien hypertexte n’est pas défini.
  
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de la cellule Address dans la boîte de dialogue **Liens hypertexte** (cliquez sur **Lien hypertexte** sous l’onglet **Insertion**).
  
Pour obtenir une référence à la cellule Address à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :
  
|**Valeur**|**Description**|
|:-----|:-----|
|Nom de cellule :  <br/> |Lien hypertexte. *nom*  . Adresse où Lien hypertexte. *nom* est le nom de la ligne Hyperlink  <br/> |

Pour obtenir une référence à la cellule Address par un nom à partir d’une autre formule ou d’un programme, à l’aide de la **propriété CellsU** , utilisez :
  
|**Valeur**|**Description**|
|:-----|:-----|
| Index de la section :  <br/> |**visSectionHyperlink** <br/> |
| Index de la ligne :  <br/> |**visRow1stHyperlink** +   *i* où *i* = 0, 1, 2... |
| Index de la cellule :  <br/> |**visHLinkAddress** <br/> |
