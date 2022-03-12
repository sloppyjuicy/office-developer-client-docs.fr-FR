---
title: ObjType, cellule (section Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm745
ms.localizationpriority: medium
ms.assetid: 3afee07b-e91a-a91c-fba2-0e3251dd6385
description: Détermine si les objets sont positionnables ou repositionnables dans les diagrammes lorsque vous utilisez la boîte de dialogue Configurer la disposition pour disposer des formes.
ms.openlocfilehash: 9ad97504ef2c00b8f86d28ddd988db2794470530
ms.sourcegitcommit: 7b410a51d1e8c97e9cce8d4aa75074162b7d9485
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/12/2022
ms.locfileid: "63448390"
---
# <a name="objtype-cell-miscellaneous-section"></a>ObjType, cellule (section Miscellaneous)

Détermine si les objets sont positionnables ou repositionnables dans les diagrammes lorsque vous utilisez la boîte de dialogue **Configurer la disposition** pour disposer des formes. 
  
|**Valeur**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
|&amp;H0  <br/> |Par défaut. L'application décide en fonction du contexte de dessin. |**visLOFlagsVisDecides** <br/> |
|&amp;H1  <br/> |La forme est positionnable. |**visLOFlagsPlacable** <br/> |
|&amp;H2  <br/> |La forme est repositionnable. Il doit s'agir d'une forme à une dimension (1D). |**visLOFlagsRoutable** <br/> |
|&amp;H4  <br/> |La forme n'est ni positionnable ni repositionnable. |**visLOFlagsDont** <br/> |
|&amp;H8  <br/> |Le groupe contient des formes positionnables ou repositionnables. |**visLOFlagsPNRGroup** <br/> |
   
## <a name="remarks"></a>Remarques

Par défaut, la cellule ObjType est définie sur No Formula, ce qui renvoie la valeur 0 ; c’est donc l’application qui détermine si la forme peut être positionnée selon son contexte. Par exemple, si vous dessinez un rectangle, la valeur de la cellule ObjType associée est 0. Si vous utilisez ensuite l’outil **Connecteur** pour relier le rectangle à une autre forme, Visio rétablit la cellule ObjType du rectangle sur la valeur 1 (positionnable). 
  
La valeur de la cellule ObjType peut être une combinaison de plusieurs valeurs. Toutefois, si le bit non positionnable est définie (&amp;H4), il est prioritaire sur les autres valeurs à l’exception de la valeur de groupe (&amp;H8).
  
Pour obtenir une référence à la cellule ObjType par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de la cellule :**  <br/> |ObjType  <br/> |
   
Pour obtenir une référence à la cellule ObjType à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRowMisc** <br/> |
|**Index de la cellule :**  <br/> |**visLOFlags** <br/> |
   

