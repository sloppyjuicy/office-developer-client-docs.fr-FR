---
title: WalkPreference, cellule (section Glue Info)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1115
ms.localizationpriority: medium
ms.assetid: 08165195-7e4e-f3ab-fa76-fbcacb0a9c9c
description: Détermine si un point de fin d'une forme 1D se déplace vers un point de connexion horizontal ou vertical sur la forme à laquelle il est collé avec de la colle dynamique, lorsque la forme est déplacée dans une position ambiguë. Par défaut, les deux points de fin d'une forme 1D se déplacent vers les points de connexion horizontaux.
ms.openlocfilehash: 5bf57a844296558ead9c906f1a63a65884df2dde
ms.sourcegitcommit: b2c5a02b2d0abd2da2542089fc3f83ff07e121e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2022
ms.locfileid: "63508233"
---
# <a name="walkpreference-cell-glue-info-section"></a>WalkPreference, cellule (section Glue Info)

Détermine si un point de fin d'une forme 1D se déplace vers un point de connexion horizontal ou vertical sur la forme à laquelle il est collé avec de la colle dynamique, lorsque la forme est déplacée dans une position ambiguë. Par défaut, les deux points de fin d'une forme 1D se déplacent vers les points de connexion horizontaux.
  
|**Valeur**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
| 1  <br/> | Le point de début de la forme 1D se déplace vers un point de connexion vertical et le point de fin, vers un point de connexion horizontal (connexions haut / bas vers côté). |**vis PremierfBegNS** <br/> |
| 2  <br/> | Le point de début de la forme 1D se déplace vers un point de connexion horizontal et le point de fin, vers un point de connexion vertical (connexions côté vers haut ou côté vers bas). |**vis PremièrePrefEndNS** <br/> |
   
## <a name="remarks"></a>Remarques

Cette cellule n'a pas d'effet sur les liens dynamiques. Le comportement d'un lien dynamique est déterminé par son style de positionnement. Reportez-vous à la cellule RouteStyle pour connaître le style de positionnement par défaut des liens dynamiques d'une page ou à la cellule ShapeRouteStyle pour le style de positionnement d'un lien dynamique donné.
  
Pour obtenir une référence à la cellule WalkPreference par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de la cellule :**  <br/> | WalkPreference  <br/> |
   
Pour obtenir une référence à la cellule WalkPreference par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowMisc** <br/> |
| **Index de la cellule :**  <br/> |**visChansPref** <br/> |
   

