---
title: AvenueSizeX, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm65
localization_priority: Normal
ms.assetid: 86fe25ed-590d-b2f0-5dfe-9746a19c6b04
description: Détermine la distance horizontale entre les formes sur la page de dessin lorsque vous les disposez à l'aide de la boîte de dialogue Configurer la disposition (sous l'onglet création, dans le groupe disposition, cliquez sur nouvelle disposition de page, puis cliquez sur autres options de disposition).
ms.openlocfilehash: 28eea2589e34c7793e89e01495eb519b987553a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411644"
---
# <a name="avenuesizex-cell-page-layout-section"></a>AvenueSizeX, cellule (section Page Layout)

Détermine la distance horizontale entre les formes sur la page de dessin lorsque vous les disposez à l'aide de la boîte de dialogue **configurer la disposition** (sous l'onglet **création** , dans le groupe **disposition** , cliquez sur **nouvelle disposition de page**, puis cliquez sur * * plus Options de disposition * *).
  
## <a name="remarks"></a>Remarques

Vous pouvez également définir cette valeur dans la boîte de dialogue **Espacement : disposition et positionnement** (sous l’onglet **Création**, cliquez sur la flèche dans le groupe **Mise en page**, cliquez sur **Disposition et positionnement**, puis sur **Espacement**).
  
La grille dynamique utilise le paramètre dans la cellule AvenueSizeX uniquement lorsqu’une forme est disponible pour calculer l’espacement horizontal. Pour utiliser la grille dynamique, dans le groupe **Aides visuelles** de l’onglet **Affichage**, activez la case à cocher **Grille dynamique**.
  
Pour obtenir une référence à la cellule AvenueSizeX par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | AvenueSizeY  <br/> |
   
Pour obtenir une référence à la cellule AvenueSizeX à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowPageLayout** <br/> |
| Index de la cellule :  <br/> |**visPLOAvenueSizeX** <br/> |
   

