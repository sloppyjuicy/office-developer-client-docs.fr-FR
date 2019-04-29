---
title: ObjType, cellule (section Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm745
localization_priority: Normal
ms.assetid: 3afee07b-e91a-a91c-fba2-0e3251dd6385
description: Détermine si les objets sont positionnables ou repositionnables dans les diagrammes lorsque vous utilisez la boîte de dialogue Configurer la disposition pour disposer des formes.
ms.openlocfilehash: 7a607fdb53ad569e84976b6f9911fbd89f7f2628
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425728"
---
# <a name="objtype-cell-miscellaneous-section"></a>ObjType, cellule (section Miscellaneous)

Détermine si les objets sont positionnables ou repositionnables dans les diagrammes lorsque vous utilisez la boîte de dialogue **Configurer la disposition** pour disposer des formes. 
  
|**Valeur**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
|&amp;H0  <br/> |Valeur par défaut. L'application décide en fonction du contexte de dessin.  <br/> |**visLOFlagsVisDecides** <br/> |
|&amp;H1  <br/> |La forme est positionnable.  <br/> |**visLOFlagsPlacable** <br/> |
|&amp;H2  <br/> |La forme est repositionnable. Il doit s'agir d'une forme à une dimension (1D).  <br/> |**visLOFlagsRoutable** <br/> |
|&amp;H4  <br/> |La forme n'est ni positionnable ni repositionnable.  <br/> |**visLOFlagsDont** <br/> |
|&amp;H8  <br/> |Le groupe contient des formes positionnables ou repositionnables.  <br/> |**visLOFlagsPNRGroup** <br/> |
   
## <a name="remarks"></a>Remarques

Par défaut, la cellule ObjType est définie sur No Formula, ce qui renvoie la valeur 0 ; c’est donc l’application qui détermine si la forme peut être positionnée selon son contexte. Par exemple, si vous dessinez un rectangle, la valeur de la cellule ObjType associée est 0. Si vous utilisez ensuite l’outil **Connecteur** pour relier le rectangle à une autre forme, Visio rétablit la cellule ObjType du rectangle sur la valeur 1 (positionnable). 
  
La valeur de la cellule ObjType peut être une combinaison de plusieurs valeurs. En revanche, si le bit non positionnable est défini&amp;(H4), il prend la priorité sur les autres valeurs à l'exception de&amp;la valeur de groupe (H8).
  
Pour obtenir une référence à la cellule ObjType par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |Déclaré  <br/> |
   
Pour obtenir une référence à la cellule ObjType à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**Définis** <br/> |
|Index de la ligne :  <br/> |**visRowMisc** <br/> |
|Index de la cellule :  <br/> |**visLOFlags** <br/> |
   

