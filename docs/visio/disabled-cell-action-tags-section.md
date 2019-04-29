---
title: Disabled, cellule (section Action Tags)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60038
localization_priority: Normal
ms.assetid: bf0a80c9-0fdb-e2cf-3ab0-74cb6338fdce
description: Indique si la balise d’action s’affiche dans la fenêtre de dessin.
ms.openlocfilehash: 867d36e27cb890509b0687500caf719362a711fb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439666"
---
# <a name="disabled-cell-action-tags-section"></a>Disabled, cellule (section Action Tags)

Indique si la balise d’action s’affiche dans la fenêtre de dessin.
  
> [!NOTE]
> Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ». 
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | La balise d’action est désactivée.  <br/> |
| FALSE  <br/> | La balise d’action est activée (valeur par défaut).  <br/> |
   
## <a name="remarks"></a>Remarques

Lorsqu’une balise d’action est désactivée, elle ne s’affiche plus du tout tant qu’elle n’est pas réactivée. 
  
Pour obtenir une référence à la cellule Disabled à partir du nom d’une autre formule ou d’un programme à l’aide de la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | SmartTag.  *nom* . Désactivé où SmartTags. *Name* est le nom de la ligne de balise d'action  <br/> |
   
Pour obtenir une référence à la cellule Disabled à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionSmartTag** <br/> |
| Index de la ligne :  <br/> |**visRowSmartTag** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visSmartTagDisabled** <br/> |
   

