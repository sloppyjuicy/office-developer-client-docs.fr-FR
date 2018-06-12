---
title: AND, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251391
localization_priority: Normal
ms.assetid: 434d7ceb-1050-c667-fb3d-b6634440c18e
description: Renvoie la valeur TRUE (1) si toutes les expressions logiques fournies sont vraies. Si une des expressions logiques est FALSE ou 0, la fonction et renvoie la valeur FALSE (0).
ms.openlocfilehash: 27b2ef97ef1d0afde37596b18674c6de26355a1b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788032"
---
# <a name="and-function"></a>AND, fonction

Renvoie la valeur TRUE (1) si toutes les expressions logiques fournies sont vraies. Si une des expressions logiques est FALSE ou 0, la fonction et renvoie la valeur FALSE (0).
  
## <a name="syntax"></a>Syntaxe

ET (** *expression1 logique* **, ** *expression2 logique* **,..., ** *expressionN logique* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _expression logique_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> | Combinaison de constantes, d’opérateurs, de fonctions et de références à des cellules ShapeSheet constituant une valeur. Toute expression donnant une valeur différente de zéro est considérée comme vraie (valeur TRUE).  <br/> |
   
## <a name="example"></a>Exemple

ET (hauteur \> 1, PinX \> 1)
  
Renvoie TRUE si les deux expressions sont vraies. Renvoie FALSE si l’une des expressions est fausse.
  

