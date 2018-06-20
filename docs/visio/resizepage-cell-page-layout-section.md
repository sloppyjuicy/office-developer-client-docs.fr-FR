---
title: ResizePage, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm850
localization_priority: Normal
ms.assetid: d63fe874-1027-3436-dbc1-73e722bce22e
description: Détermine si la page pour inclure le dessin après la disposition des formes à l’aide de la boîte de dialogue Configurer la disposition est agrandie (sous l’onglet Création, dans le groupe mise en page, cliquez sur Re-mise en Page, puis cliquez sur autres Options de mise en page).
ms.openlocfilehash: fab37ee4561ba82ea1f314ad595e513253478b30
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789476"
---
# <a name="resizepage-cell-page-layout-section"></a>ResizePage, cellule (section Page Layout)

Détermine si la page pour inclure le dessin après la disposition des formes à l’aide de la boîte de dialogue **Configurer la disposition** est agrandie (sous l’onglet **Création** , dans le groupe **mise en page** , cliquez sur **Re-mise en** Page, puis cliquez sur **plus de mise en page Options de**).
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | La page est agrandie.  <br/> |
| FALSE  <br/> | La page n'est pas agrandie.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule ResizePage par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | ResizePage  <br/> |
   
Pour obtenir une référence à la cellule ResizePage par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowPageLayout** <br/> |
| Index de la cellule :  <br/> |**visPLOResizePage** <br/> |
   

