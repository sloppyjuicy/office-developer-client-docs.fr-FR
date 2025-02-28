---
title: ButtonFace, cellule (section Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60025
ms.localizationpriority: medium
ms.assetid: cf15b879-a47e-a5a5-bfdd-1d7ea423742f
description: Identifie l’icône qui s’affiche en regard d’une option de menu contextuel ou de balise d’action.
ms.openlocfilehash: 6a05a73173ac73cebcebb17ed679dca8ddab3b84
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63404714"
---
# <a name="buttonface-cell-actions-section"></a>ButtonFace, cellule (section Actions)

Identifie l’icône qui s’affiche en regard d’une option de menu contextuel ou de balise d’action.
  
> [!NOTE]
> Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ». 
  
## <a name="remarks"></a>Remarques

La chaîne contenue dans la cellule ButtonFace représente l'ID d'une image de bouton Microsoft Office. Une valeur de zéro (0) ou vide indique qu'aucune icône ne s'affiche. 
  
Les ID utilisables dans la cellule ButtonFace sont les mêmes que ceux utilisés avec la propriété **FaceID** d'un objet **CommandBarButton**. Pour plus d’informations sur ces ID, recherchez « Working with command bar button images » sur MSDN. 
  
Pour obtenir une référence à la cellule ButtonFace à partir du nom d’une autre formule ou d’un programme à l’aide de la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de cellule :**  <br/> |**Actions**.  *nom*  . **ButtonFace où** **Actions**.  *name*  est le nom de la ligne actions  <br/> |
   
Pour obtenir une référence à la cellule ButtonFace par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionAction** <br/> |
|**Index de la ligne :**  <br/> |**visRowAction** +   *i* où **i** = 0, 1, 2... |
|**Index de la cellule :**  <br/> |**visActionButtonFace** <br/> |
   

