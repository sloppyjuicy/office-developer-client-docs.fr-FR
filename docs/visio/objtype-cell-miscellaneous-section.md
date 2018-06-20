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
ms.openlocfilehash: 23887e1d265e9e5ac1dfa9750bab65e8428b1c76
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789195"
---
# <a name="objtype-cell-miscellaneous-section"></a>ObjType, cellule (section Miscellaneous)

Détermine si les objets sont positionnables ou repositionnables dans les diagrammes lorsque vous utilisez la boîte de dialogue **Configurer la disposition** pour disposer des formes. 
  
|**Valeur**|**Description**|**Constante d’Automation**|
|:-----|:-----|:-----|
|&amp;H0  <br/> |Par défaut. L'application décide en fonction du contexte de dessin.  <br/> |**visLOFlagsVisDecides** <br/> |
|&amp;H1  <br/> |La forme est positionnable.  <br/> |**visLOFlagsPlacable** <br/> |
|&amp;H2  <br/> |La forme est repositionnable. Il doit s'agir d'une forme à une dimension (1D).  <br/> |**visLOFlagsRoutable** <br/> |
|&amp;H4  <br/> |La forme n'est ni positionnable ni repositionnable.  <br/> |**visLOFlagsDont** <br/> |
|&amp;H8  <br/> |Le groupe contient des formes positionnables ou repositionnables.  <br/> |**visLOFlagsPNRGroup** <br/> |
   
## <a name="remarks"></a>Remarques

Par défaut, la cellule ObjType est définie sur aucune formule d’une forme, prend la valeur 0, ce qui signifie que l’application détermine si la forme peut être positionnable en fonction de son contexte. Par exemple, si vous dessinez un rectangle, la valeur de la cellule ObjType associée est 0. Si vous utilisez ensuite l’outil **connecteur** pour relier le rectangle à une autre forme, Visio rétablit la valeur de la cellule ObjType du rectangle 1 (positionnable). 
  
La valeur de la cellule ObjType peut être une combinaison de valeurs. Si le bit non positionnable est défini (&amp;H4), toutefois, il est prioritaire sur les autres valeurs, à l’exception de la valeur de groupe (&amp;H8).
  
Pour obtenir une référence à la cellule ObjType par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |Type de l’objet  <br/> |
   
Pour obtenir une référence à la cellule ObjType par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowMisc** <br/> |
|Index de la cellule :  <br/> |**visLOFlags** <br/> |
   

