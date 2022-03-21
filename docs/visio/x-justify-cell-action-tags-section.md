---
title: X Justify, cellule (section Action Tags)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1026936
ms.localizationpriority: medium
ms.assetid: a8995020-3eaa-2b2c-eca0-dd475de4d06f
description: Décalage x du bouton de balise d’action par rapport au point défini par les cellules X et Y.
ms.openlocfilehash: bc9a2f258c7e1e161b4a560225baa716a8ec622b
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63630965"
---
# <a name="x-justify-cell-action-tags-section"></a>X Justify Cell (Action Tags Section)

Décalage *x*  du bouton de balise d’action par rapport au point défini par les cellules X et Y. 
  
> [!NOTE]
> Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ». 
  
|**Valeur**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
| 0  <br/> | Aligné à gauche (valeur par défaut). |**visSmartTagXJustifyLeft** <br/> |
| 1  <br/> | Centré. |**visSmartTagXJustifyCenter** <br/> |
| 2  <br/> | Aligné à droite. |**visSmartTagXJustifyRight** <br/> |
   
## <a name="remarks"></a>Remarques

Les cellules X Justify et Y Justify déterminent où le bouton de balise d’action est placé par rapport au point défini dans les cellules X et Y. 
  
Pour obtenir une référence à la cellule X Justify à partir du nom d’une autre formule ou d’un programme à partir de la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | SmartTags.  *nom*  . XJustify où SmartTags. *name est*  le nom de la ligne de balise d’action  <br/> |
   
Pour obtenir une référence à la cellule X Justify par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionSmartTag** <br/> |
| **Index de la ligne :**  <br/> |**visRowSmartTag** +   *i* où *i* = 0, 1, 2... |
| **Index de la cellule :**  <br/> |**visSmartTagXJustify** <br/> |
   

