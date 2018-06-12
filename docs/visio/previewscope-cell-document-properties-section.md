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
ms.openlocfilehash: 865da052f710481c146d3c2692ddf506018be789
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789344"
---
# <a name="previewscope-cell-document-properties-section"></a>PreviewScope, cellule (section Document Properties)

Détermine si le dessin inclut un aperçu. Si c'est le cas, cette cellule détermine également si l'aperçu ne représente que la première page du dessin ou toutes ses pages.
  
|**Valeur**|**Portée de l’aperçu**|**Constante d’Automation**|
|:-----|:-----|:-----|
| 0  <br/> | Première page  <br/> |**visDocPreviewScope1stPage** <br/> |
| 1  <br/> | Aucune  <br/> |**visDocPreviewScopeNone** <br/> |
| 2  <br/> | Toutes les pages  <br/> |**visDocPreviewScopeAllPages** <br/> |
   
## <a name="remarks"></a>Note

Vous pouvez également définir cette valeur sur l’onglet **Résumé** de la boîte de dialogue **Propriétés** (cliquez sur le bouton **Office** , cliquez sur l’onglet **Infos** , cliquez sur **Propriétés du Document**, puis cliquez sur **Propriétés avancées**).
  
Pour obtenir une référence à la cellule PreviewScope par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | PreviewScope  <br/> |
   
Pour obtenir une référence à la cellule PreviewScope par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowDoc** <br/> |
| Index de la cellule :  <br/> |**visDocPreviewScope** <br/> |
   

