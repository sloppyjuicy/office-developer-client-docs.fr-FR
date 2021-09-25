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
ms.openlocfilehash: 96610ad6e1add550ab6ed940b7dc2ccbfb8373da
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608612"
---
# <a name="buttonface-cell-actions-section"></a>ButtonFace, cellule (section Actions)

Identifie l’icône qui s’affiche en regard d’une option de menu contextuel ou de balise d’action.
  
> [!NOTE]
> Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ». 
  
## <a name="remarks"></a>Remarques

La chaîne contenue dans la cellule ButtonFace représente l'ID d'une image de bouton Microsoft Office. Une valeur de zéro (0) ou vide indique qu'aucune icône ne s'affiche. 
  
Les ID utilisables dans la cellule ButtonFace sont les mêmes que ceux utilisés avec la propriété **FaceID** d'un objet **CommandBarButton**. Pour plus d’informations sur ces ID, recherchez « Working with command bar button images » sur MSDN. 
  
Pour obtenir une référence à la cellule ButtonFace à partir du nom d’une autre formule ou d’un programme à l’aide de la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |**Actions**.  *nom*  . **ButtonFace où** **Actions**.  *name*  est le nom de la ligne actions  <br/> |
   
Pour obtenir une référence à la cellule ButtonFace par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionAction** <br/> |
|Index de la ligne :  <br/> |**visRowAction**  +   *i* où **i** = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visActionButtonFace** <br/> |
   

