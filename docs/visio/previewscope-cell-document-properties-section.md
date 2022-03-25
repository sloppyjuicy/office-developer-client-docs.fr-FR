---
title: PreviewScope, cellule (section Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm820
ms.localizationpriority: medium
ms.assetid: d03ae1b3-da6c-56d3-4f96-6e131c04e93e
description: Détermine si le dessin inclut un aperçu. Si c'est le cas, cette cellule détermine également si l'aperçu ne représente que la première page du dessin ou toutes ses pages.
ms.openlocfilehash: 34f669228ba884c3db864c581279f4e03906586d
ms.sourcegitcommit: eb9453e5664b01759b602cb5a4cef5b4885128f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2022
ms.locfileid: "63782740"
---
# <a name="previewscope-cell-document-properties-section"></a>PreviewScope, cellule (section Document Properties)

Détermine si le dessin inclut un aperçu. Si c'est le cas, cette cellule détermine également si l'aperçu ne représente que la première page du dessin ou toutes ses pages.
  
|**Valeur**|**Portée de l'aperçu**|**Constante d'automation**|
|:-----|:-----|:-----|
| 0  <br/> | Première page  <br/> |**visDocPreviewScope1stPage** <br/> |
| 1  <br/> | Aucun  <br/> |**visDocPreviewScopeNone** <br/> |
| 2  <br/> | Toutes les pages  <br/> |**visDocPreviewScopeAllPages** <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir cette valeur sous l’onglet Résumé dans la  boîte de dialogue Propriétés (cliquez sur le bouton **Office**, sur l’onglet Informations, sur Propriétés du **document**, puis sur Propriétés  **avancées).**
  
Pour obtenir une référence à la cellule PreviewScope par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|Étiquette|Valeur|
|:-----|:-----|
| Nom de la cellule :  <br/> | PreviewScope  <br/> |
   
Pour obtenir une référence à la cellule PreviewScope à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|Index|Argument|
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowDoc** <br/> |
| Index de la cellule :  <br/> |**visDocPreviewScope** <br/> |
   

