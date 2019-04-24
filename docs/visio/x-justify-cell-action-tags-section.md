---
title: X Justify, cellule (section Action Tags)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1026936
localization_priority: Normal
ms.assetid: a8995020-3eaa-2b2c-eca0-dd475de4d06f
description: Décalage x du bouton de balise d'action par rapport au point défini par les cellules X et Y.
ms.openlocfilehash: f8542d2f3a22b12794d999323d202d7a5bece20b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284971"
---
# <a name="x-justify-cell-action-tags-section"></a>X Justify Cell (Action Tags Section)

Décalage *x* du bouton de balise d'action par rapport au point défini par les cellules X et Y. 
  
> [!NOTE]
> Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ». 
  
|**Value**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
| 0  <br/> | Aligné à gauche (valeur par défaut).  <br/> |**visSmartTagXJustifyLeft** <br/> |
| 0,1  <br/> | Centré.  <br/> |**visSmartTagXJustifyCenter** <br/> |
| n°2  <br/> | Aligné à droite.  <br/> |**visSmartTagXJustifyRight** <br/> |
   
## <a name="remarks"></a>Remarques

Les cellules X Justify et Y Justify déterminent le positionnement du bouton de balise d'action par rapport au point défini dans les cellules X et Y. 
  
Pour obtenir une référence à la cellule X Justify à partir du nom d’une autre formule ou d’un programme à partir de la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | SmartTag.  *nom* . XJustify où SmartTags. *Name* est le nom de la ligne de balise d'action  <br/> |
   
Pour obtenir une référence à la cellule X Justify par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionSmartTag** <br/> |
| Index de la ligne :  <br/> |**visRowSmartTag** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visSmartTagXJustify** <br/> |
   

