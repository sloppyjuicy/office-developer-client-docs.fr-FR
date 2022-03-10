---
title: AvenueSizeX, cellule (section Page Layout)
manager: lindalu
ms.date: 03/09/2022
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm65
ms.localizationpriority: medium
ms.assetid: 86fe25ed-590d-b2f0-5dfe-9746a19c6b04
description: Détermine la quantité d’espace horizontal entre les formes sur la page de dessin lorsque vous les avez mises en page à l’aide de la boîte de dialogue Configurer la disposition.
ms.openlocfilehash: 6ae51d18198a1518b7ffe22fb50104bd0c36957f
ms.sourcegitcommit: 4164855836af53a068bbbc5b5d126f83ee83e324
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2022
ms.locfileid: "63427195"
---
# <a name="avenuesizex-cell-page-layout-section"></a>AvenueSizeX, cellule (section Page Layout)

Détermine la quantité d’espace horizontal entre les formes de la page de dessin lorsque vous les avez mises en page à l’aide de la boîte  de dialogue Configurer la disposition  (sous l’onglet Création, dans le groupe Disposition, cliquez sur **Re-disposition** de la page, puis cliquez sur Autres **options** de disposition).
  
## <a name="remarks"></a>Remarques

Vous pouvez également définir cette valeur dans la boîte de dialogue **Espacement : disposition et positionnement** (sous l’onglet **Création**, cliquez sur la flèche dans le groupe **Mise en page**, cliquez sur **Disposition et positionnement**, puis sur **Espacement**).
  
La grille dynamique utilise le paramètre dans la cellule AvenueSizeX uniquement lorsqu’une forme est disponible pour calculer l’espacement horizontal. Pour utiliser la grille dynamique, dans le groupe **Aides visuelles** de l’onglet **Affichage**, activez la case à cocher **Grille dynamique**.
  
Pour obtenir une référence à la cellule AvenueSizeX par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez :
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | AvenueSizeY  <br/> |

Pour obtenir une référence à la cellule AvenueSizeX à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowPageLayout** <br/> |
| **Index de la cellule :**  <br/> |**visPLOAvenueSizeX** <br/> |
