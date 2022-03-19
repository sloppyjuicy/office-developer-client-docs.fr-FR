---
title: ResizePage, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm850
ms.localizationpriority: medium
ms.assetid: d63fe874-1027-3436-dbc1-73e722bce22e
description: Détermine si la page doit être agrandie pour inclure le dessin après la disposition automatique des formes à l’aide de la boîte de dialogue Configurer la disposition (sous l’onglet Création, dans le groupe Disposition, cliquez sur Nouvelle disposition de page, puis cliquez sur Autres options de disposition).
ms.openlocfilehash: fb59775bce77de76f1f9617354c80f806bf710c4
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63633735"
---
# <a name="resizepage-cell-page-layout-section"></a>ResizePage, cellule (section Page Layout)

Détermine s’il faut agrandir la page pour entourer le dessin après la disposition des formes à l’aide de la boîte de dialogue Configurer  la disposition (sous l’onglet Création, dans le groupe Disposition, cliquez sur Nouvelle **disposition de page**, puis cliquez sur Autres **options** de disposition). 
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | La page est agrandie. |
| FALSE  <br/> | La page n'est pas agrandie. |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule ResizePage par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de la cellule :**  <br/> | ResizePage  <br/> |
   
Pour obtenir une référence à la cellule ResizePage à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowPageLayout** <br/> |
| **Index de la cellule :**  <br/> |**visPLOResizePage** <br/> |
   

