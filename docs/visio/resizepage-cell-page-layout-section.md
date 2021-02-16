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
description: Détermine si la page doit être agrandie pour inclure le dessin après la disposition automatique des formes à l’aide de la boîte de dialogue Configurer la disposition (sous l’onglet Création, dans le groupe Disposition, cliquez sur Nouvelle disposition de page, puis cliquez sur Autres options de disposition).
ms.openlocfilehash: 8d0001ce35808f8c5f11068ed78865ce992af5cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438091"
---
# <a name="resizepage-cell-page-layout-section"></a>ResizePage, cellule (section Page Layout)

Détermine s’il faut agrandir la page pour entourer le  dessin après la disposition  des formes  à l’aide de la boîte de dialogue Configurer la disposition (sous l’onglet Création, dans le groupe Disposition, cliquez sur Nouvelle disposition **de** page, puis cliquez sur Autres **options** de disposition).
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | La page est agrandie.  <br/> |
| FALSE  <br/> | La page n'est pas agrandie.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule ResizePage par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | ResizePage  <br/> |
   
Pour obtenir une référence à la cellule ResizePage à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowPageLayout** <br/> |
| Index de la cellule :  <br/> |**visPLOResizePage** <br/> |
   

