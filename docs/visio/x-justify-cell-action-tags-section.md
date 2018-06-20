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
description: Le - décalage x du bouton de balise d’action par rapport au point défini par les cellules X et Y.
ms.openlocfilehash: 043d7b198ae5a529c623545fb54ef5aa1d32217d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790058"
---
# <a name="x-justify-cell-action-tags-section"></a>X Justify, cellule (section Action Tags)

*X* -décalage du bouton de balise d’action par rapport au point défini par les cellules X et Y. 
  
> [!NOTE]
> Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ». 
  
|**Valeur**|**Description**|**Constante d’Automation**|
|:-----|:-----|:-----|
| 0  <br/> | Aligné à gauche (valeur par défaut).  <br/> |**visSmartTagXJustifyLeft** <br/> |
| 1  <br/> | Centré.  <br/> |**visSmartTagXJustifyCenter** <br/> |
| 2  <br/> | Aligné à droite.  <br/> |**visSmartTagXJustifyRight** <br/> |
   
## <a name="remarks"></a>Remarques

Les cellules X Justify et Y Justify déterminent où se trouve le bouton de balise d’action par rapport au point défini dans les cellules X et Y. 
  
Pour obtenir une référence à la cellule X Justify par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Balises actives.  *nom* . XJustify où SmartTags. *nom* est le nom de la ligne de balise d’action  <br/> |
   
Pour obtenir une référence à la cellule X Justify par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionSmartTag** <br/> |
| Index de la ligne :  <br/> |**visRowSmartTag** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visSmartTagXJustify** <br/> |
   

