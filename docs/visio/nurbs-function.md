---
title: NURBS, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251579
localization_priority: Normal
ms.assetid: f34db20d-6501-2026-a5e8-29c4d4cb2405
description: Renvoie une courbe B-spline rationnelle (NURBS). Cette fonction est utilisée dans la cellule E dans les lignes de géométrie NURBSTo.
ms.openlocfilehash: 005a66b9da2425beaf416ec2273c10446c183add
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19789211"
---
# <a name="nurbs-function"></a>NURBS, fonction

Renvoie une courbe B-spline rationnelle (NURBS). Cette fonction est utilisée dans la cellule E dans les lignes de géométrie NURBSTo.
  
## <a name="syntax"></a>Syntaxe

NURBS (** *dernier nœud* **, ** *degré* **, ** *xType* **, ** *yType* **, ** *x1* **, ** *y1* **, ** *nœud1* **, ** *épaisseur1* **,...) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _dernier nœud_ <br/> |Obligatoire  <br/> |**string** <br/> | Dernier nœud  <br/> |
| _degré_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Degré de la courbe Spline  <br/> |
| _xType_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Spécifie comment interpréter les données _x_ entrées. Si _xType_ a la valeur 0, toutes les données d’entrée _x_ est interprétée comme un pourcentage de largeur. Si _xType_ a la valeur 1, toutes les données d’entrée _x_ est interprétée comme des coordonnées locales.  <br/> |
| _yType_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Spécifie comment interpréter les données _y_ entrées. Si _yType_ a la valeur 0, toutes les données entrées _y_ est interprétée comme un pourcentage de hauteur. Si _yType_ a la valeur 1, toutes les données entrées _y_ est interprétée comme des coordonnées locales.  <br/> |
| _x1_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Coordonnée x  <br/> |
| _y1_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Coordonnée y  <br/> |
| _Nœud1_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Nœud sur la courbe B-spline  <br/> |
| _épaisseur1_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Épaisseur sur la courbe B-spline  <br/> |
   
## <a name="remarks"></a>Note

Pour chaque argument *x* , il doit exister un argument *y* ; dans le cas contraire, une erreur est renvoyée. 
  
Vous devez spécifier au moins un *x*, *y*, *nœud* et *épaisseur* argument ; dans le cas contraire, Visio renvoie une erreur. 
  

