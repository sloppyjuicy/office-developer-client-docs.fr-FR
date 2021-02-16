---
title: GlueType, cellule (section Glue Info)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm420
localization_priority: Normal
ms.assetid: fffbefd6-8b0b-0023-6b03-026d1c6e885e
description: Détermine si une forme 1D utilise un collage statique (point à point) ou dynamique (forme à forme) lorsqu'elle est attachée à une autre forme.
ms.openlocfilehash: ae4eddf17c6e7b5e56cb3397f03d0721d965c9b7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410671"
---
# <a name="gluetype-cell-glue-info-section"></a>GlueType, cellule (section Glue Info)

Détermine si une forme 1D utilise un collage statique (point à point) ou dynamique (forme à forme) lorsqu'elle est attachée à une autre forme.
  
|**Valeur**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
| &amp;H0  <br/> | Par défaut. Utilise le collage dynamique uniquement pour les connecteurs dynamiques. Utilise le collage statique dans les autres cas.  <br/> |**visGlueTypeDefault** <br/> |
| &amp;H1  <br/> | Autorise le collage dynamique.  <br/> | Obsolète dans Visio 2002  <br/> |
| &amp;H2  <br/> | Autorise le collage dynamique.  <br/> |**visGlueTypeTaping** <br/> |
| &amp;H4  <br/> | N'autorise pas le collage dynamique.  <br/> |**visGlueTypeNo Quinging** <br/> |
| &amp;H8  <br/> | N'autorise pas le collage dynamique de cette forme 2D.  <br/> |**visGlueTypeNo QuingTo** <br/> |
   
## <a name="remarks"></a>Remarques

Si cette cellule contient la valeur 1, 2 ou 3, le collage dynamique sera utilisé dans les cas suivants :
  
- Les formes sont collées de façon dynamique dans l'interface utilisateur.
    
- Les formes sont collées à la cellule AxeX ou AxeY d'une autre forme à partir d'un programme.
    
Si les formes sont collées à des cellules autres que AxeX ou AxeY d'une forme à partir d'un programme, le collage statique est utilisé.
  
Lorsque la valeur de cette cellule change et ne permet plus le collage dynamique, les attaches dynamiques existantes ne sont pas modifiées ni rompues. Les programmes peuvent établir un collage dynamique même s'il est désactivé dans la cellule GlueType.
  
Pour obtenir une référence à la cellule GlueType par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | GlueType  <br/> |
   
Pour obtenir une référence à la cellule GlueType à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowMisc** <br/> |
| Index de la cellule :  <br/> |**visGlueType** <br/> |
   

