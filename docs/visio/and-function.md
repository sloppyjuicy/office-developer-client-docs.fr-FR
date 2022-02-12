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
description: Renvoie TRUE (1) si toutes les expressions logiques fournies sont TRUE. Si l’une des expressions logiques est FALSE ou 0, la fonction AND renvoie FALSE (0).
ms.openlocfilehash: 99c1c5e4fbde4570352376294b889d741d578037
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62774621"
---
# <a name="and-function"></a>Fonction AND

Renvoie TRUE (1) si toutes les expressions logiques fournies sont TRUE. Si l’une des expressions logiques est FALSE ou 0, la fonction AND renvoie FALSE (0).
  
## <a name="syntax"></a>Syntaxe

AND(** *logical expression1* **, ** *logical expression2* **,..., ** *logical expressionN* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _expression logique_ <br/> |Requis  <br/> |**String** <br/> | Combinaison de constantes, d’opérateurs, de fonctions et de références à des cellules ShapeSheet constituant une valeur. Toute expression donnant une valeur différente de zéro est considérée comme vraie (valeur TRUE). |
   
## <a name="example"></a>Exemple

AND(Height \> 1, PinX \> 1)
  
Renvoie TRUE si les deux expressions sont vraies. Renvoie FALSE si l’une des expressions est fausse.
  

