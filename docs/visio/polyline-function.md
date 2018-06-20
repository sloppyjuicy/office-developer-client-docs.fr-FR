---
title: POLYLINE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251576
localization_priority: Normal
ms.assetid: 10baeec9-6c9b-b4ba-3138-7d1156a9e056
description: Renvoie une polyligne. Cette fonction est utilisée dans la cellule A de PolyligneVers géométrie.
ms.openlocfilehash: afe31b3963cca03d0273b8768f6cc5538d1850ee
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789258"
---
# <a name="polyline-function"></a>POLYLINE, fonction

Renvoie une polyligne. Cette fonction est utilisée dans la cellule A de PolyligneVers géométrie. 
  
## <a name="syntax"></a>Syntaxe

POLYLINE (** *xType* **, ** *yType* **, ** *x1* **, ** *y1* **...) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _xType_ <br/> |Obligatoire  <br/> |**Boolean** <br/> |Spécifie comment interpréter les données _x_ entrées. Si _xType_ a la valeur 0, l’entrée _x_-données sont interprétées comme un pourcentage de largeur. Si _xType_ a la valeur 1, l’entrée _x_-données sont interprétées comme une coordonnée locale.  <br/> |
| _yType_ <br/> |Obligatoire  <br/> |**Boolean** <br/> |Spécifie comment interpréter les _y_-saisie. Si _yType_ a la valeur 0, l’entrée _y_-données sont interprétées comme un pourcentage de hauteur. Si _yType_ a la valeur 1, l’entrée _y_-données sont interprétées comme une coordonnée locale.  <br/> |
| _x1_ <br/> |Obligatoire  <br/> |**Number** <br/> | _X_-coordonner.  <br/> |
| _y1_ <br/> |Obligatoire  <br/> |**Number** <br/> |_Y_-coordonner.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour chaque argument *x* , il doit exister un argument *y* ; dans le cas contraire, une erreur est renvoyée. 
  
## <a name="example"></a>Exemple

POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0) 
  
Renvoie un rectangle de dimensions Largeur x Hauteur. 
  

