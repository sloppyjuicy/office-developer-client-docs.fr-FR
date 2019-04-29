---
title: Y Dynamics, cellule (section Controls)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251284
localization_priority: Normal
ms.assetid: cb221974-2f1a-edb0-477b-39a3c4a64c56
description: Représente la coordonnée y du point d'ancrage d'une poignée de contrôle, exprimée dans le système de coordonnées locales. Le point d'ancrage est utilisé pour l'étirement dynamique des formes.
ms.openlocfilehash: 13d463ebccd9cc7a23641a036dc5dd967513b07f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404826"
---
# <a name="y-dynamics-cell-controls-section"></a>Y Dynamics, cellule (section Controls)

Représente la coordonnée *y* du point d'ancrage d'une poignée de contrôle, exprimée dans le système de coordonnées locales. Le point d'ancrage est utilisé pour l'étirement dynamique des formes. 
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Y Dynamics par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Vérifie.  *nom* . Contrôles YDynwhere.  *Name* est le nom de la ligne Controls.  <br/> |
   
Pour obtenir une référence à la cellule Y Dynamics par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionControls** <br/> |
| Index de la ligne :  <br/> |**visRowControl** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visCtlYDyn** <br/> |
   

