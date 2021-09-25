---
title: Rounding, cellule (section Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm860
ms.localizationpriority: medium
ms.assetid: c44457ca-997a-5315-44dd-4218e4203550
description: Indique le rayon de l'arrondi qui est appliqué lorsque deux segments contigus d'un chemin se rejoignent. Par exemple, l'arrondi permet d'attribuer des angles arrondis à un rectangle. Pour le définir, entrez une valeur associée à des unités de mesure (une paire nombre-unité).
ms.openlocfilehash: 8012422c654b3090ee2c007ce8911e53eef28cfd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607793"
---
# <a name="rounding-cell-line-format-section"></a>Rounding, cellule (section Line Format)

Indique le rayon de l'arrondi qui est appliqué lorsque deux segments contigus d'un chemin se rejoignent. Par exemple, l'arrondi permet d'attribuer des angles arrondis à un rectangle. Pour le définir, entrez une valeur associée à des unités de mesure (une paire nombre-unité).
  
## <a name="remarks"></a>Remarques

Vous pouvez également définir  cette valeur dans  la boîte de  dialogue Trait (sous l’onglet Accueil, dans le groupe Formes, cliquez sur **Trait,** pointez sur **Poids,** puis cliquez sur **Autres** lignes).
  
Pour obtenir une référence à la cellule Rounding par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |Arrondi  <br/> |
   
Pour obtenir une référence à la cellule Rounding à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowLine** <br/> |
|Index de la cellule :  <br/> |**visLineRounding** <br/> |
   

