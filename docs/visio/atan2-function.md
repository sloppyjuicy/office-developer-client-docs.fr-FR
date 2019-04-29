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
description: Renvoie l'angle entre le vecteur représenté par x, y et la direction de l'axe des abscisses. Le résultat est un nombre exprimé dans l’unité actuelle de mesure des angles.
ms.openlocfilehash: 906c024f2a78d6e11c1bbf770c14d04299cadca8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436481"
---
# <a name="atan2-function"></a>Fonction ATAN2

Renvoie l'angle entre le vecteur représenté par *x, y* et la direction de l' ** axe des abscisses. Le résultat est un nombre exprimé dans l’unité actuelle de mesure des angles. 
  
## <a name="syntax"></a>Syntaxe

ATAN2 (* * *y* * *, * * *x* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _y_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Valeur _y_du point.  <br/> |
| _x_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Valeur _x_du point.  <br/> |
   
## <a name="remarks"></a>Remarques

L'arctangente est l'angle mesuré dans le sens des aiguilles d'une passe à partir de l'axe *x* positif vers une ligne qui coupe l'origine (0,0) et le point représenté par *x* et *y* . Dans Microsoft Visio, ATAN2(0,0) renvoie 0. Pour exprimer le résultat de la fonction ATAN2 dans une unité de mesure d’angle différente, utilisez les fonctions DEG ou RAD. 
  
La fonction ATAN2 est l'antifonction de la fonction TAN. La fonction ATAN2 renvoie l'angle dont l'angle est égal à *y* divisé par *x* . Si ATAN2 (*y, x*) représente un angle dans un triangle droit, *y* le «côté opposé» et *x* le «côté adjacent», de sorte que la fonction peut être écrite sous la forme atan2 (opposé, adjacent). 
  
## <a name="example-1"></a>Exemple 1

ATAN2 (1,25, 2,25)
  
Renvoie 29,0456 deg
  
## <a name="example-2"></a>Exemple 2

ATAN2 (1, SQRT (3))
  
Renvoie 30 deg
  
## <a name="example-3"></a>Exemple 3

ATAN2 (1,1)
  
Renvoie 45 deg
  

