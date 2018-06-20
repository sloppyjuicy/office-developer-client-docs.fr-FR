---
title: ATAN2, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251397
localization_priority: Normal
ms.assetid: 524278fb-196e-9cf9-e27b-d03642beeee4
description: Renvoie l’angle entre le vecteur représenté par x, y et la direction de la x-axe. Le résultat est un nombre dans l’unité actuelle de mesure pour les angles.
ms.openlocfilehash: dfd62ce628a3a46ff14b3ffc3f07074a39c66e14
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788018"
---
# <a name="atan2-function"></a>ATAN2, fonction

Renvoie l’angle entre le vecteur représenté par *x, y* et la direction de la *x* -axe. Le résultat est un nombre dans l’unité actuelle de mesure pour les angles. 
  
## <a name="syntax"></a>Syntaxe

ATAN2 (** *y* **, ** *x* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _y_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |La valeur _y_-valeur du point.  <br/> |
| _x_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |_X_-valeur du point.  <br/> |
   
## <a name="remarks"></a>Remarques

L’arctangente est l’angle mesuré dans le sens inverse de la *x* positif-axe sur une ligne qui coupe l’origine (0,0) et le point représenté par les valeurs *x* et *y* . Dans Microsoft Visio, ATAN2 (0,0) renvoie 0. Pour forcer le résultat de la fonction ATAN2 dans une mesure d’angle différente, utilisez les fonctions DEG ou RAD. 
  
La fonction ATAN2 est la fonction inverse de la fonction TAN. La fonction ATAN2 renvoie l’angle dont angle est égale à *y* divisé par *x* . Si ATAN2 (*y, x*) représente un angle dans un triangle, *y* est le « côté opposé » et *x* étant le « côté adjacent », la fonction peut être écrite comme ATAN2(opposite,adjacent). 
  
## <a name="example-1"></a>Exemple 1

ATAN2(1.25,2.25)
  
Renvoie 29,0456 deg
  
## <a name="example-2"></a>Exemple 2

ATAN2(1,RACINE(3))
  
Renvoie 30 deg
  
## <a name="example-3"></a>Exemple 3

ATAN2(1,1)
  
Renvoie 45 deg
  

