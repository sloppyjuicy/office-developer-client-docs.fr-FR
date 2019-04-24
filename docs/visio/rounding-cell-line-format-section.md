---
title: Rounding, cellule (section Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm860
localization_priority: Normal
ms.assetid: c44457ca-997a-5315-44dd-4218e4203550
description: Indique le rayon de l'arrondi qui est appliqué lorsque deux segments contigus d'un chemin se rejoignent. Par exemple, l'arrondi permet d'attribuer des angles arrondis à un rectangle. Pour le définir, entrez une valeur associée à des unités de mesure (une paire nombre-unité).
ms.openlocfilehash: d64d3266e3dd2b0a3998955efe271aab04905fbf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358582"
---
# <a name="rounding-cell-line-format-section"></a>Rounding, cellule (section Line Format)

Indique le rayon de l'arrondi qui est appliqué lorsque deux segments contigus d'un chemin se rejoignent. Par exemple, l'arrondi permet d'attribuer des angles arrondis à un rectangle. Pour le définir, entrez une valeur associée à des unités de mesure (une paire nombre-unité).
  
## <a name="remarks"></a>Remarques

Vous pouvez également définir cette valeur dans la boîte de dialogue **trait** (sous l'onglet **Accueil** , dans le groupe **forme** , cliquez sur **trait**, pointez sur **poids**, puis cliquez sur **autres traits**).
  
Pour obtenir une référence à la cellule Rounding par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |Arrondi  <br/> |
   
Pour obtenir une référence à la cellule Rounding à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**Définis** <br/> |
|Index de la ligne :  <br/> |**visRowLine** <br/> |
|Index de la cellule :  <br/> |**visLineRounding** <br/> |
   

