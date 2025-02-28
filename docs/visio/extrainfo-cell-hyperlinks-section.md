---
title: ExtraInfo, cellule (section Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm360
ms.localizationpriority: medium
ms.assetid: 55834445-8619-f79a-aea0-0f6a1780e016
description: Représente une chaîne qui passe l'information à utiliser dans la résolution d'une URL, comme les coordonnées d'un point dans une image interactive. Par exemple, dans la cellule ExtraInfo, x=41y&amp;=7 indique les coordonnées d’une carte image.
ms.openlocfilehash: d59f94407de6c1ce69cce8d66db1b29c58ce343f
ms.sourcegitcommit: b2c5a02b2d0abd2da2542089fc3f83ff07e121e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2022
ms.locfileid: "63507819"
---
# <a name="extrainfo-cell-hyperlinks-section"></a>ExtraInfo, cellule (section Hyperlinks)

Représente une chaîne qui passe l'information à utiliser dans la résolution d'une URL, comme les coordonnées d'un point dans une image interactive. Par exemple, dans la cellule ExtraInfo, « x=41y&amp;=7 » spécifie les coordonnées d’un plan d’image.
  
## <a name="remarks"></a>Remarques

Les cellules Event ne sont évaluées que lorsque l'événement se produit, et non lors de l'entrée de la formule.
  
Pour obtenir une référence à la cellule ExtraInfo par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | Lien hypertexte.  *nom*  . ExtraInfo où Lien hypertexte.  *nom est*  le nom de ligne  <br/> |
   
Pour obtenir une référence à la cellule ExtraInfo à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionHyperlink** <br/> |
| **Index de la ligne :**  <br/> |**visRow1stHyperlink** +   *i* où *i* = 0, 1, 2... |
| **Index de la cellule :**  <br/> |**visHLinkExtraInfo** <br/> |
   

