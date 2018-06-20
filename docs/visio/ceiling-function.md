---
title: CEILING, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251405
localization_priority: Normal
ms.assetid: 1a8d6d48-7ae3-5483-28d2-5b1706088a53
description: Arrondit un nombre éloignée de 0 (zéro) à l’occurrence suivante du dénominateur. Si plusieurs n’est pas spécifié, le nombre est arrondi éloignée de 0 à l’entier.
ms.openlocfilehash: fa982b44ea4a73e7da614c49a52cd50efd612f20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788201"
---
# <a name="ceiling-function"></a>CEILING, fonction

Arrondit un nombre éloignée de 0 (zéro) à l’occurrence suivante de _multiple_. Si _plusieurs_ n’est pas spécifié, le nombre est arrondi éloignée de 0 à l’entier. 
  
## <a name="syntax"></a>Syntaxe

CEILING (** *numéro* **, ** *plusieurs* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatoire  <br/> |**Number** <br/> |Nombre à arrondir.  <br/> |
| _plusieurs_ <br/> |Obligatoire  <br/> |**Number** <br/> |Plusieurs à arrondir à.  <br/> |
   
## <a name="remarks"></a>Remarques

 _Nombre_ et _plusieurs_ doivent avoir le même signe, sinon une #NUM ! erreur est renvoyée. Si _nombre_ ou _multiple_ ne peut pas être convertie en une valeur, un #VALUE ! erreur est renvoyée. Si le _nombre_ ou le _multiple_ est égal à 0, le résultat est 0. 
  
## <a name="example-1"></a>Exemple 1

CEILING(3.7)
  
Renvoie 4
  
## <a name="example-2"></a>Exemple 2

CEILING(-3.7)
  
Renvoie -4
  
## <a name="example-3"></a>Exemple 3

CEILING (3.7, 0,25)
  
Renvoie 3,75
  

