---
title: AND, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251391
ms.localizationpriority: medium
ms.assetid: 434d7ceb-1050-c667-fb3d-b6634440c18e
description: Renvoie TRUE (1) si toutes les expressions logiques fournies sont true. Si l’une des expressions logiques est FALSE ou 0, la fonction AND renvoie FALSE (0).
ms.openlocfilehash: 82ce384641c400764356d3288ae7d903ee901292
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628877"
---
# <a name="and-function"></a>Fonction AND

Renvoie TRUE (1) si toutes les expressions logiques fournies sont true. Si l’une des expressions logiques est FALSE ou 0, la fonction AND renvoie FALSE (0).
  
## <a name="syntax"></a>Syntaxe

AND(** *logical expression1* **, ** *logical expression2* **,..., ** *logical expressionN* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _expression logique_ <br/> |Obligatoire  <br/> |**String** <br/> | Combinaison de constantes, d’opérateurs, de fonctions et de références à des cellules ShapeSheet constituant une valeur. Toute expression donnant une valeur différente de zéro est considérée comme vraie (valeur TRUE).  <br/> |
   
## <a name="example"></a>Exemple

AND(Height \> 1, PinX \> 1)
  
Renvoie TRUE si les deux expressions sont vraies. Renvoie FALSE si l’une des expressions est fausse.
  

