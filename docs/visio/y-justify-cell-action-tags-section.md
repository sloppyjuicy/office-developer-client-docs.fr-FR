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
ms.openlocfilehash: d996e0976afc8c739ac91a8d78a6145620e37e68
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63376377"
---
# <a name="y-justify-cell-action-tags-section"></a>Y Justify, cellule (section Action Tags)

Décalage *y*  du bouton de balise d’action par rapport au point défini par les cellules X et Y.
  
> [!NOTE]
> Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ».
  
|**Valeur**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
| 0  <br/> | Aligné en haut (valeur par défaut). |**visSmartTagYJustifyTop** <br/> |
| 1  <br/> | Centré. |**visSmartTagYJustifyMiddle** <br/> |
| 2  <br/> | Aligné en bas. |**visSmartTagYJustifyBottom** <br/> |

## <a name="remarks"></a>Remarques

Les cellules X Justify et Y Justify déterminent où le bouton de balise d’action est placé par rapport au point défini dans les cellules X et Y.
  
Pour obtenir une référence à la cellule Y Justify par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | SmartTags. *nom* . YJustify où SmartTags. *nom* est le nom de la ligne de balise d’action.  <br/> |

Pour obtenir une référence à la cellule Y Justify par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionSmartTag** <br/> |
| Index de la ligne :  <br/> |**visRowSmartTag** +   *i* où *i* = 0, 1, 2... |
| Index de la cellule :  <br/> |**visSmartTagYJustify** <br/> |
