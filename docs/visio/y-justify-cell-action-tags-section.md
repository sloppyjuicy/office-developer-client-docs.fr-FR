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
description: La valeur y-décalage du bouton de balise d’action par rapport au point défini par les cellules X et Y.
ms.openlocfilehash: 8f8323d1f392654bf118ece2f78890f2a1b860ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790088"
---
# <a name="y-justify-cell-action-tags-section"></a>Y Justify, cellule (section Action Tags)

La valeur *y* -décalage du bouton de balise d’action par rapport au point défini par les cellules X et Y. 
  
> [!NOTE]
> Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ». 
  
|**Valeur**|**Description**|**Constante d’Automation**|
|:-----|:-----|:-----|
| 0  <br/> | Aligné en haut (valeur par défaut).  <br/> |**visSmartTagYJustifyTop** <br/> |
| 1  <br/> | Centré.  <br/> |**visSmartTagYJustifyMiddle** <br/> |
| 2  <br/> | Aligné en bas.  <br/> |**visSmartTagYJustifyBottom** <br/> |
   
## <a name="remarks"></a>Remarques

Les cellules X Justify et Y Justify déterminent où se trouve le bouton de balise d’action par rapport au point défini dans les cellules X et Y.
  
Pour obtenir une référence à la cellule Y Justify par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Balises actives.  *nom* . YJustify où SmartTags. *nom* est le nom de la ligne de balise d’action  <br/> |
   
Pour obtenir une référence à la cellule Y Justify par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionSmartTag** <br/> |
| Index de la ligne :  <br/> |**visRowSmartTag** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visSmartTagYJustify** <br/> |
   

