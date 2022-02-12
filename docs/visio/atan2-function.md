---
title: ATAN2, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251397
ms.localizationpriority: medium
ms.assetid: 524278fb-196e-9cf9-e27b-d03642beeee4
description: Renvoie l’angle entre le vecteur représenté par x,y et la direction de l’axe des x. Le résultat est un nombre exprimé dans l’unité actuelle de mesure des angles.
ms.openlocfilehash: 8c91175d0110e584d782c27a151debafc02a7b47
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62787519"
---
# <a name="atan2-function"></a>Fonction ATAN2

Renvoie l’angle entre le vecteur représenté par  *x,y*  et la direction de  *l’axe des x*  . Le résultat est un nombre exprimé dans l’unité actuelle de mesure des angles. 
  
## <a name="syntax"></a>Syntaxe

ATAN2(** *y* **, ** *x* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _y_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Valeur  _y_ du point. |
| _x_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Valeur  _x_ du point. |
   
## <a name="remarks"></a>Remarques

L’arcange est l’angle mesuré dans le sens inverse des aiguilles d’une montre, de l’axe  *des x*  positifs à une ligne qui coupe l’origine (0,0) et le point représenté par  *x*  et  *y*  . Dans Microsoft Visio, ATAN2(0,0) renvoie 0. Pour exprimer le résultat de la fonction ATAN2 dans une unité de mesure d’angle différente, utilisez les fonctions DEG ou RAD. 
  
La fonction ATAN2 est la fonction antifonction de la fonction TAN. La fonction ATAN2 renvoie l’angle dont l’angle est égal à  *y*  divisé par  *x*  . Si ATAN2(*y,x*) représente un angle dans un triangle droit,  *y*  est le « côté opposé » et  *x*  le « côté adjacent », de sorte que la fonction peut être écrite en tant que ATAN2(opposé,adjacent). 
  
## <a name="example-1"></a>Exemple 1

ATAN2(1.25,2.25)
  
Renvoie 29,0456 deg
  
## <a name="example-2"></a>Exemple 2

ATAN2(1,SQRT(3))
  
Renvoie 30 deg
  
## <a name="example-3"></a>Exemple 3

ATAN2(1,1)
  
Renvoie 45 deg
  

