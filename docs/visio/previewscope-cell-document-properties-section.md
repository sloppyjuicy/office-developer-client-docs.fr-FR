---
title: PreviewScope, cellule (section Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm820
localization_priority: Normal
ms.assetid: d03ae1b3-da6c-56d3-4f96-6e131c04e93e
description: Détermine si le dessin inclut un aperçu. Si c'est le cas, cette cellule détermine également si l'aperçu ne représente que la première page du dessin ou toutes ses pages.
ms.openlocfilehash: 34dbc9ac02032b2cb5cb6373c3c6361e3d822312
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356111"
---
# <a name="previewscope-cell-document-properties-section"></a>PreviewScope, cellule (section Document Properties)

Détermine si le dessin inclut un aperçu. Si c'est le cas, cette cellule détermine également si l'aperçu ne représente que la première page du dessin ou toutes ses pages.
  
|**Valeur**|**Portée de l'aperçu**|**Constante d'automation**|
|:-----|:-----|:-----|
| 0  <br/> | Première page  <br/> |**visDocPreviewScope1stPage** <br/> |
| 0,1  <br/> | Aucun  <br/> |**visDocPreviewScopeNone** <br/> |
| n°2  <br/> | Toutes les pages  <br/> |**visDocPreviewScopeAllPages** <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir cette valeur sous l'onglet **Résumé** de la boîte de dialogue **Propriétés** (cliquez sur le bouton **Office** , cliquez sur l'onglet **informations** , cliquez sur **Propriétés du document**, puis cliquez sur **Propriétés avancées**).
  
Pour obtenir une référence à la cellule PreviewScope par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | PreviewScope  <br/> |
   
Pour obtenir une référence à la cellule PreviewScope à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowDoc** <br/> |
| Index de la cellule :  <br/> |**visDocPreviewScope** <br/> |
   

