---
title: Disabled, cellule (section Action Tags)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60038
ms.localizationpriority: medium
ms.assetid: bf0a80c9-0fdb-e2cf-3ab0-74cb6338fdce
description: Indique si la balise d’action s’affiche dans la fenêtre de dessin.
ms.openlocfilehash: a2bcb4f66109e155b5c5504008ea10059c6d283f
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62771628"
---
# <a name="disabled-cell-action-tags-section"></a>Disabled, cellule (section Action Tags)

Indique si la balise d’action s’affiche dans la fenêtre de dessin.
  
> [!NOTE]
> Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ». 
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | La balise d’action est désactivée. |
| FALSE  <br/> | La balise d’action est activée (valeur par défaut). |
   
## <a name="remarks"></a>Remarques

Lorsqu’une balise d’action est désactivée, elle ne s’affiche plus du tout tant qu’elle n’est pas réactivée. 
  
Pour obtenir une référence à la cellule Disabled à partir du nom d’une autre formule ou d’un programme à l’aide de la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | SmartTags.  *nom*  . Désactivé lorsque SmartTags. *name est*  le nom de la ligne de balise d’action  <br/> |
   
Pour obtenir une référence à la cellule Disabled à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionSmartTag** <br/> |
| Index de la ligne :  <br/> |**visRowSmartTag** +   *i* où *i* = 0, 1, 2... |
| Index de la cellule :  <br/> |**visSmartTagDisabled** <br/> |
   

