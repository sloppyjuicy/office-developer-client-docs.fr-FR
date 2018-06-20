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
ms.openlocfilehash: b96ad4a877d72bf4457ec3cf038a29a2b414e0f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789664"
---
# <a name="shapeshdwtype-cell-fill-format-section"></a>ShapeShdwType, cellule (section Fill Format)

Indique le type d'ombre d'une forme. 
  
|**Valeur**|**Description**|**Constante d’Automation**|
|:-----|:-----|:-----|
|0  <br/> |Utiliser la valeur par défaut de la page (valeur par défaut)  <br/> |**visFSTPageDefault** <br/> |
|1  <br/> |Simple  <br/> |**visFSTSimple** <br/> |
|2  <br/> |Oblique  <br/> |**visFSTOblique** <br/> |
   
## <a name="remarks"></a>Remarques

Utilisez cette cellule pour appliquer une ombre de la forme qui est différente de la page par défaut (le type d’ombre page par défaut est défini dans la cellule ShdwType dans la Section Page Properties).
  
Types d’ombre simple sont décrits comme des ombres décalage dans l’interface utilisateur (IU). Une ombre simple donne l’effet de la forme de son ombre portée sur un plan parallèle situé derrière la forme. Ombres obliques sont décrites comme telles dans l’interface utilisateur et donnent l’effet d’une ombre portée sur un plan perpendiculaire à la forme. 
  
Pour obtenir la liste des types d’ombre simples et obliques prédéfinis, reportez-vous à la zone de **Style** dans la boîte de dialogue **ombre** (sous l’onglet **accueil** , dans le groupe **forme** , cliquez sur **ombre**, puis cliquez sur **Options d’ombres**).
  
Pour obtenir une référence à la cellule ShapeShdwType par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |ShapeShdwType  <br/> |
   
Pour obtenir une référence à la cellule ShapeShdwType par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowFill** <br/> |
|Index de la cellule :  <br/> |**visFillShdwType** <br/> |
   

