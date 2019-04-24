---
title: ShapeShdwType, cellule (section Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033173
localization_priority: Normal
ms.assetid: 1461148d-90a9-6f7c-1b28-9310ffaf0e3b
description: Indique le type d'ombre d'une forme.
ms.openlocfilehash: 607881e4a520f1376562394c6e40ab5d2508906d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342860"
---
# <a name="shapeshdwtype-cell-fill-format-section"></a>ShapeShdwType Cell (Fill Format Section)

Indique le type d'ombre d'une forme. 
  
|**Value**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
|0  <br/> |Utiliser la valeur par défaut de la page (valeur par défaut)  <br/> |**visFSTPageDefault** <br/> |
|0,1  <br/> |Simple  <br/> |**visFSTSimple** <br/> |
|n°2  <br/> |Italique  <br/> |**visFSTOblique** <br/> |
   
## <a name="remarks"></a>Remarques

Utilisez cette cellule pour appliquer une ombre de forme différente de celle par défaut de la page (le type d'ombre par défaut de la page est défini dans la cellule ShdwType de la section Propriétés de la page).
  
Les ombres simples sont décrites comme des ombres de décalage dans l'interface utilisateur. Une ombre simple donne l'impression que la forme a son ombre portée sur un plan parallèle situé derrière elle. Les ombres obliques sont décrites comme telles dans l'interface utilisateur et donnent l'impression d'une ombre portée sur un plan perpendiculaire à la forme. 
  
Pour obtenir une liste de types d’ombre simples et obliques prédéfinis, reportez-vous à la zone **Style** dans la boîte de dialogue **Ombre** (sous l’onglet **Accueil**, dans le groupe **Forme**, cliquez sur **Ombre**, puis cliquez sur **Options d’ombres**).
  
Pour obtenir une référence à la cellule ShapeShdwType par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |ShapeShdwType  <br/> |
   
Pour obtenir une référence à la cellule ShapeShdwType à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**Définis** <br/> |
|Index de la ligne :  <br/> |**visRowFill** <br/> |
|Index de la cellule :  <br/> |**visFillShdwType** <br/> |
   

