---
title: Blur, cellule (section Image Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm115
ms.localizationpriority: medium
ms.assetid: 8b077cdb-6036-4f77-dc20-a476bb75b0f7
description: Estompe ou adoucit une image bitmap. La valeur par défaut est 0 %.
ms.openlocfilehash: 5c592ec5feb24efd87bdbb827a90e22fb5971557
ms.sourcegitcommit: b2c5a02b2d0abd2da2542089fc3f83ff07e121e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2022
ms.locfileid: "63506117"
---
# <a name="blur-cell-image-properties-section"></a>Blur, cellule (section Image Properties)

Estompe ou adoucit une image bitmap. La valeur par défaut est 0 %.
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Blur par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de la cellule :**  <br/> | Flou  <br/> |
   
Pour obtenir une référence à la cellule Blur à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowImage** <br/> |
| **Index de la cellule :**  <br/> |**visImageBlur** <br/> |
   

