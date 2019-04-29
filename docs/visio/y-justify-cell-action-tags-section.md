---
title: Y Justify, cellule (section Action Tags)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1026937
localization_priority: Normal
ms.assetid: 27042b62-7623-95d7-7e10-f589d74605c7
description: Offset y du bouton de balise d'action par rapport au point défini par les cellules X et Y.
ms.openlocfilehash: d7a1f5c1feda3624c9f96039e7247c737a91a813
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419981"
---
# <a name="y-justify-cell-action-tags-section"></a>Y Justify, cellule (section Action Tags)

Offset *y* du bouton de balise d'action par rapport au point défini par les cellules X et y. 
  
> [!NOTE]
> Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ». 
  
|**Valeur**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
| 0  <br/> | Aligné en haut (valeur par défaut).  <br/> |**visSmartTagYJustifyTop** <br/> |
| 0,1  <br/> | Centré.  <br/> |**visSmartTagYJustifyMiddle** <br/> |
| n°2  <br/> | Aligné en bas.  <br/> |**visSmartTagYJustifyBottom** <br/> |
   
## <a name="remarks"></a>Remarques

Les cellules X Justify et Y Justify déterminent le positionnement du bouton de balise d'action par rapport au point défini dans les cellules X et Y.
  
Pour obtenir une référence à la cellule Y Justify par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | SmartTag.  *nom* . YJustify où SmartTags. *Name* est le nom de la ligne de balise d'action  <br/> |
   
Pour obtenir une référence à la cellule Y Justify par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionSmartTag** <br/> |
| Index de la ligne :  <br/> |**visRowSmartTag** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visSmartTagYJustify** <br/> |
   

