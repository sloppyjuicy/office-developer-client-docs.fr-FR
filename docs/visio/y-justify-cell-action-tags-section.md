---
title: Y Justify, cellule (section Action Tags)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1026937
ms.localizationpriority: medium
ms.assetid: 27042b62-7623-95d7-7e10-f589d74605c7
description: Décalage y du bouton de balise d’action par rapport au point défini par les cellules X et Y.
ms.openlocfilehash: 2a06a0fc889ea5e88526da5656550050b5f46d08
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59581698"
---
# <a name="y-justify-cell-action-tags-section"></a>Y Justify, cellule (section Action Tags)

Décalage  *y*  du bouton de balise d’action par rapport au point défini par les cellules X et Y. 
  
> [!NOTE]
> Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ». 
  
|**Valeur**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
| 0  <br/> | Aligné en haut (valeur par défaut).  <br/> |**visSmartTagYJustifyTop** <br/> |
| 1  <br/> | Centré.  <br/> |**visSmartTagYJustifyMiddle** <br/> |
| 2  <br/> | Aligné en bas.  <br/> |**visSmartTagYJustifyBottom** <br/> |
   
## <a name="remarks"></a>Remarques

Les cellules X Justify et Y Justify déterminent où le bouton de balise d’action est placé par rapport au point défini dans les cellules X et Y.
  
Pour obtenir une référence à la cellule Y Justify par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | SmartTags.  *nom*  . YJustify où SmartTags. *name est*  le nom de la ligne de balise d’action  <br/> |
   
Pour obtenir une référence à la cellule Y Justify par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionSmartTag** <br/> |
| Index de la ligne :  <br/> |**visRowSmartTag**  +   *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visSmartTagYJustify** <br/> |
   

