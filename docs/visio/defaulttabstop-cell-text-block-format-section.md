---
title: DefaultTabstop, cellule (section Text Block Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm220
ms.localizationpriority: medium
ms.assetid: 3b3e458a-206c-8699-8bf7-da80f4350706
description: Détermine l’intervalle des taquets de tabulation par défaut dans un bloc de texte.
ms.openlocfilehash: cd075e82d5c7e3fbd8f7ab381f472ca0d91eccd7
ms.sourcegitcommit: b2c5a02b2d0abd2da2542089fc3f83ff07e121e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2022
ms.locfileid: "63506545"
---
# <a name="defaulttabstop-cell-text-block-format-section"></a>DefaultTabstop, cellule (section Text Block Format)

Détermine l’intervalle des taquets de tabulation par défaut dans un bloc de texte. 
  
## <a name="remarks"></a>Remarques

La valeur par défaut est de 1,5 cm pour les documents créés en unités métriques et de 0,5 pouce pour ceux créés en unités impériales.
  
Pour obtenir une référence à la cellule DefaultTabstop par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de cellule :**  <br/> |DefaultTabstop  <br/> |
   
Pour obtenir une référence à la cellule DefaultTabstop à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRowText** <br/> |
|**Index de la cellule :**  <br/> |**visTxtBlkDefaultTabStop** <br/> |
   

