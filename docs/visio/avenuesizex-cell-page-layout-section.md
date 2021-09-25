---
title: AvenueSizeX, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm65
ms.localizationpriority: medium
ms.assetid: 86fe25ed-590d-b2f0-5dfe-9746a19c6b04
description: Détermine la quantité d’espace horizontal entre les formes de la page de dessin lorsque vous les avez mises en page à l’aide de la boîte de dialogue Configurer la disposition (sous l’onglet Création, dans le groupe Disposition, cliquez sur Re-Layout Page, puis sur Autres options de disposition).
ms.openlocfilehash: 99bdeaee634211bbb8e300d8981b8cd66be379cd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603892"
---
# <a name="avenuesizex-cell-page-layout-section"></a>AvenueSizeX, cellule (section Page Layout)

Détermine la quantité d’espace horizontal entre les formes sur la page de dessin lorsque  vous les  avez mises en page à l’aide de la boîte de dialogue Configurer la disposition (sous l’onglet Création, dans le groupe Disposition, cliquez sur Nouvelle disposition **de page,** puis cliquez sur ** Autres options de disposition **). 
  
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
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowPageLayout** <br/> |
| Index de la cellule :  <br/> |**visPLOAvenueSizeX** <br/> |
   

